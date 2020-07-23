---
title: 'Diagnose in den Q # Standard-Bibliotheken'
description: 'Erfahren Sie mehr über die Diagnosefunktionen und-Vorgänge in den Q # Standard-Bibliotheken, die zum Abfangen von Fehlern oder Fehlern in quantenprogrammen verwendet werden'
author: cgranade
uid: microsoft.quantum.libraries.diagnostics
ms.author: chgranad@microsoft.com
ms.topic: article
ms.openlocfilehash: 324753cfa1b7d940bf5a0bbe7665f19cc6dda82c
ms.sourcegitcommit: cdf67362d7b157254e6fe5c63a1c5551183fc589
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/21/2020
ms.locfileid: "86870633"
---
# <a name="diagnostics"></a><span data-ttu-id="f9118-103">Diagnose</span><span class="sxs-lookup"><span data-stu-id="f9118-103">Diagnostics</span></span> #

<span data-ttu-id="f9118-104">Wie bei der klassischen Entwicklung ist es wichtig, dass Sie Fehler und Fehler in quantumprogrammen diagnostizieren können.</span><span class="sxs-lookup"><span data-stu-id="f9118-104">As with classical development, it is important to be able to diagnose mistakes and errors in quantum programs.</span></span>
<span data-ttu-id="f9118-105">Die Q #-Standardbibliotheken bieten eine Vielzahl verschiedener Möglichkeiten, um die Richtigkeit von quantenprogrammen sicherzustellen, wie in beschrieben <xref:microsoft.quantum.guide.testingdebugging> .</span><span class="sxs-lookup"><span data-stu-id="f9118-105">The Q# standard libraries provide a variety of different ways to ensure the correctness of quantum programs, as detailed in <xref:microsoft.quantum.guide.testingdebugging>.</span></span>
<span data-ttu-id="f9118-106">Diese Unterstützung wird größtenteils in Form von Funktionen und Vorgängen bereitgestellt, die entweder den Zielcomputer anweisen, zusätzliche Diagnoseinformationen für das Host Programm oder den Entwickler bereitzustellen, oder die Richtigkeit der Bedingungen und invarianten erzwingen, die durch den Funktions-oder Vorgangs Aufrufsatz ausgedrückt werden.</span><span class="sxs-lookup"><span data-stu-id="f9118-106">Largely speaking, this support comes in the form of functions and operations that either instruct the target machine to provide additional diagnostic information to the host program or developer, or enforce the correctness of conditions and invariants expressed by the function or operation call.</span></span>

## <a name="machine-diagnostics"></a><span data-ttu-id="f9118-107">Computer Diagnose</span><span class="sxs-lookup"><span data-stu-id="f9118-107">Machine Diagnostics</span></span> ##

<span data-ttu-id="f9118-108">Die Diagnose von klassischen Werten kann mithilfe der-Funktion abgerufen werden <xref:microsoft.quantum.intrinsic.message> , um eine Nachricht auf Computer abhängige Weise zu protokollieren.</span><span class="sxs-lookup"><span data-stu-id="f9118-108">Diagnostics about classical values can be obtained by using the <xref:microsoft.quantum.intrinsic.message> function to log a message in a machine-dependent way.</span></span>
<span data-ttu-id="f9118-109">Standardmäßig wird die Zeichenfolge in die Konsole geschrieben.</span><span class="sxs-lookup"><span data-stu-id="f9118-109">By default, this writes the string to the console.</span></span>
<span data-ttu-id="f9118-110">Wird in Verbindung mit interinterpolierten Zeichen folgen verwendet und <xref:microsoft.quantum.intrinsic.message> erleichtert das Melden von Diagnoseinformationen über klassische Werte:</span><span class="sxs-lookup"><span data-stu-id="f9118-110">Used together with interpolated strings, <xref:microsoft.quantum.intrinsic.message> makes it easy to report diagnostic information about classical values:</span></span>

```Q#
let angle = Microsoft.Quantum.Math.PI() * 2.0 / 3.0;
Message($"About to rotate by an angle of {angle}...");
```

> [!NOTE]
> <span data-ttu-id="f9118-111">`Message`weist eine Signatur auf `(String -> Unit)` , die wiederum darstellt, dass die Ausgabe einer Debugprotokollierung nicht innerhalb von Q # beobachtet werden kann.</span><span class="sxs-lookup"><span data-stu-id="f9118-111">`Message` has signature `(String -> Unit)`, again representing that emitting a debug log message cannot be observed from within Q#.</span></span>

<span data-ttu-id="f9118-112">Die <xref:microsoft.quantum.diagnostics.dumpmachine> <xref:microsoft.quantum.diagnostics.dumpregister> callables und weisen Zielcomputer an, Diagnoseinformationen zu allen derzeit zugeordneten Qubits bzw. zu einem bestimmten Register von Qubits bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="f9118-112">The <xref:microsoft.quantum.diagnostics.dumpmachine> and <xref:microsoft.quantum.diagnostics.dumpregister> callables instruct target machines to provide diagnostic information about all currently allocated qubits or about a specific register of qubits, respectively.</span></span>
<span data-ttu-id="f9118-113">Jeder Zielcomputer variiert in Abhängigkeit von den Diagnoseinformationen, die als Reaktion auf eine dumpanweisung bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="f9118-113">Each target machine varies in what diagnostic information is provided in response to a dump instruction.</span></span>
<span data-ttu-id="f9118-114">Der Zielcomputer des [vollständigen Zustands Simulators](xref:microsoft.quantum.machines.full-state-simulator) stellt beispielsweise dem Host Programm den Zustands Vektor bereit, den er intern zur Darstellung eines Register von Qubits verwendet.</span><span class="sxs-lookup"><span data-stu-id="f9118-114">The [full state simulator](xref:microsoft.quantum.machines.full-state-simulator) target machine, for instance, provides the host program with the state vector that it uses internally to represent a register of qubits.</span></span>
<span data-ttu-id="f9118-115">Im Vergleich dazu stellt der Zielcomputer des Dienst Bereitstellungs- [Simulators](xref:microsoft.quantum.machines.toffoli-simulator) für jedes Qubit ein einzelnes klassisches Bit bereit.</span><span class="sxs-lookup"><span data-stu-id="f9118-115">By comparison, the [Toffoli simulator](xref:microsoft.quantum.machines.toffoli-simulator) target machine provides a single classical bit for each qubit.</span></span>

 <span data-ttu-id="f9118-116">Weitere Informationen zur Ausgabe des [vollständigen Zustands Simulators](xref:microsoft.quantum.machines.full-state-simulator) `DumpMachine` finden Sie im Abschnitt Dumpfunktionen in unserem [Artikel zum Testen und Debuggen](xref:microsoft.quantum.guide.testingdebugging#dump-functions).</span><span class="sxs-lookup"><span data-stu-id="f9118-116">To learn more about the [full state simulator's](xref:microsoft.quantum.machines.full-state-simulator) `DumpMachine` output, take a look at the dump functions section of our [testing and debugging article](xref:microsoft.quantum.guide.testingdebugging#dump-functions).</span></span>


## <a name="facts-and-assertions"></a><span data-ttu-id="f9118-117">Fakten und Assertionen</span><span class="sxs-lookup"><span data-stu-id="f9118-117">Facts and Assertions</span></span> ##

<span data-ttu-id="f9118-118">Wie unter [Testen und Debuggen](xref:microsoft.quantum.guide.testingdebugging)erläutert, kann eine Funktion oder ein Vorgang mit der Signatur `Unit -> Unit` `Unit => Unit` bzw. als Komponenten *Test*gekennzeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="f9118-118">As discussed in [Testing and Debugging](xref:microsoft.quantum.guide.testingdebugging), a function or operation with signature `Unit -> Unit` or `Unit => Unit`, respectively, can be marked as a *unit test*.</span></span>
<span data-ttu-id="f9118-119">Jeder Komponenten Test besteht in der Regel aus einem kleinen Quantum-Programm zusammen mit einer oder mehreren Bedingungen, die die Richtigkeit des Programms überprüfen.</span><span class="sxs-lookup"><span data-stu-id="f9118-119">Each unit test generally consists of a small quantum program, along with one or more conditions that check the correctness of that program.</span></span>
<span data-ttu-id="f9118-120">Diese Bedingungen können in Form von _Fakten_ _auftreten, die_die Werte Ihrer Eingaben überprüfen, oder Assertionen, die die Zustände von einem oder mehreren als Eingabe übergebenen Qubits überprüfen.</span><span class="sxs-lookup"><span data-stu-id="f9118-120">These conditions can come in the form of either _facts_, which check the values of their inputs, or _assertions_, which check the states of one or more qubits passed as input.</span></span>

<span data-ttu-id="f9118-121">Beispielsweise `EqualityFactI(1 + 1, 2, "1 + 1 != 2")` stellt die mathematische Tatsache dar, dass $1 + 1 = $2, während `AssertQubit(One, qubit)` die Bedingung darstellt, die die Messung `qubit` `One` mit Sicherheit zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="f9118-121">For example, `EqualityFactI(1 + 1, 2, "1 + 1 != 2")` represents the mathematical fact that $1 + 1 = 2$, while `AssertQubit(One, qubit)` represents the condition that measuring `qubit` will return a `One` with certainty.</span></span>
<span data-ttu-id="f9118-122">Im ersten Fall können wir die Richtigkeit der Bedingung nur anhand ihrer Werte überprüfen, während wir im letzteren Fall etwas über den Zustand des Qubit wissen müssen, um die Aussage auszuwerten.</span><span class="sxs-lookup"><span data-stu-id="f9118-122">In the former case, we can check the correctness of the condition given only its values, while in the latter, we must know something about the state of the qubit in order to evaluate the assertion.</span></span>

<span data-ttu-id="f9118-123">Die Q # Standard-Bibliotheken bieten verschiedene Funktionen für die Darstellung von Fakten, einschließlich:</span><span class="sxs-lookup"><span data-stu-id="f9118-123">The Q# standard libraries provide several different functions for representing facts, including:</span></span>

- <xref:microsoft.quantum.diagnostics.fact>
- <xref:microsoft.quantum.diagnostics.equalitywithintolerancefact>
- <xref:microsoft.quantum.diagnostics.nearequalityfactc>
- <xref:microsoft.quantum.diagnostics.equalityfacti>


### <a name="testing-qubit-states"></a><span data-ttu-id="f9118-124">Testen von Qubit-Zuständen</span><span class="sxs-lookup"><span data-stu-id="f9118-124">Testing Qubit States</span></span> ###

<span data-ttu-id="f9118-125">In der Praxis basieren Assertionen auf der Tatsache, dass klassische Simulationen von Quantum-Mechanismen das [No-Klon-Theorem](https://arxiv.org/abs/quant-ph/9607018)nicht einhalten müssen, sodass wir bei der Verwendung eines Simulators für den Zielcomputer nicht physische Messungen und Assertionen durchführen können.</span><span class="sxs-lookup"><span data-stu-id="f9118-125">In practice, assertions rely on the fact that classical simulations of quantum mechanics need not obey the [no-cloning theorem](https://arxiv.org/abs/quant-ph/9607018), such that we can make unphysical measurements and assertions when using a simulator for our target machine.</span></span>
<span data-ttu-id="f9118-126">Daher können wir einzelne Vorgänge auf einem klassischen Simulator testen, bevor Sie auf Hardware bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="f9118-126">Thus, we can test individual operations on a classical simulator before deploying on hardware.</span></span>
<span data-ttu-id="f9118-127">Auf Ziel Computern, die keine Auswertung von Assertionen zulassen, können Aufrufe von <xref:microsoft.quantum.diagnostics.assertmeasurement> problemlos ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="f9118-127">On target machines which do not allow evaluation of assertions, calls to <xref:microsoft.quantum.diagnostics.assertmeasurement> can be safely ignored.</span></span>

<span data-ttu-id="f9118-128">Im allgemeinen <xref:microsoft.quantum.diagnostics.assertmeasurement> wird durch den Vorgang bestätigt, dass das Messen der angegebenen Qubits in der angegebenen Pauli-Basis immer das angegebene Ergebnis hat.</span><span class="sxs-lookup"><span data-stu-id="f9118-128">More generally, the <xref:microsoft.quantum.diagnostics.assertmeasurement> operation asserts that measuring the given qubits in the given Pauli basis will always have the given result.</span></span>
<span data-ttu-id="f9118-129">Wenn die-Übersetzung fehlschlägt, wird die Ausführung beendet, indem `fail` mit der angegebenen Meldung aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="f9118-129">If the assertion fails, the execution ends by calling `fail` with the given message.</span></span>
<span data-ttu-id="f9118-130">Standardmäßig ist dieser Vorgang nicht implementiert. Simulatoren, die diese unterstützen können, sollten eine Implementierung bereitstellen, die eine Lauf Zeit Überprüfung ausführt.</span><span class="sxs-lookup"><span data-stu-id="f9118-130">By default, this operation is not implemented; simulators that can support it should provide an implementation that performs runtime checking.</span></span>
<span data-ttu-id="f9118-131">`AssertMeasurement`hat die Signatur `((Pauli[], Qubit[], Result, String) -> ())` .</span><span class="sxs-lookup"><span data-stu-id="f9118-131">`AssertMeasurement` has signature `((Pauli[], Qubit[], Result, String) -> ())`.</span></span>
<span data-ttu-id="f9118-132">Da `AssertMeasurement` eine Funktion mit einem leeren Tupel als Ausgabetyp ist, sind keine Auswirkungen des Aufrufs `AssertMeasurement` in einem Q #-Programm Observable-Ausdrücke.</span><span class="sxs-lookup"><span data-stu-id="f9118-132">Since `AssertMeasurement` is a function with an empty tuple as its output type, no effects from having called `AssertMeasurement` are observable within a Q# program.</span></span>

<span data-ttu-id="f9118-133">Die <xref:microsoft.quantum.diagnostics.assertmeasurementprobability> Vorgangs Funktion bestätigt, dass das Messen der angegebenen Qubits in der angegebenen Pauli-Basis das angegebene Ergebnis mit der angegebenen Wahrscheinlichkeit innerhalb einiger Toleranz hat.</span><span class="sxs-lookup"><span data-stu-id="f9118-133">The <xref:microsoft.quantum.diagnostics.assertmeasurementprobability> operation function asserts that measuring the given qubits in the given Pauli basis will have the given result with the given probability, within some tolerance.</span></span>
<span data-ttu-id="f9118-134">Toleranz ist additiv (z. b. `abs(expected-actual) < tol` ).</span><span class="sxs-lookup"><span data-stu-id="f9118-134">Tolerance is additive (e.g. `abs(expected-actual) < tol`).</span></span>
<span data-ttu-id="f9118-135">Wenn die-Übersetzung fehlschlägt, wird die Ausführung beendet, indem `fail` mit der angegebenen Meldung aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="f9118-135">If the assertion fails, the execution ends by calling `fail` with the given message.</span></span>
<span data-ttu-id="f9118-136">Standardmäßig ist dieser Vorgang nicht implementiert. Simulatoren, die diese unterstützen können, sollten eine Implementierung bereitstellen, die eine Lauf Zeit Überprüfung ausführt.</span><span class="sxs-lookup"><span data-stu-id="f9118-136">By default, this operation is not implemented; simulators that can support it should provide an implementation that performs runtime checking.</span></span>
<span data-ttu-id="f9118-137">`AssertMeasurementProbability`hat die Signatur `((Pauli[], Qubit[], Result, Double, String, Double) -> Unit)` .</span><span class="sxs-lookup"><span data-stu-id="f9118-137">`AssertMeasurementProbability` has signature `((Pauli[], Qubit[], Result, Double, String, Double) -> Unit)`.</span></span> <span data-ttu-id="f9118-138">Der erste `Double` Parameter gibt die gewünschte Wahrscheinlichkeit des Ergebnisses und der zweite die Toleranz an.</span><span class="sxs-lookup"><span data-stu-id="f9118-138">The first of `Double` parameters gives the desired probability of the result, and the second one the tolerance.</span></span>

<span data-ttu-id="f9118-139">Wir können mehr als Assert-Vorgänge durchführen, indem wir die klassischen Informationen verwenden, die von einem Simulator verwendet werden, um den internen Zustand eines Qubit darzustellen, sodass es nicht erforderlich ist, um unsere Assertionen zu testen.</span><span class="sxs-lookup"><span data-stu-id="f9118-139">We can do more than assert a single measurement, using that the classical information used by a simulator to represent the internal state of a qubit is amenable to copying, such that we do not need to actually perform a measurement to test our assertion.</span></span>
<span data-ttu-id="f9118-140">Dies ermöglicht es uns insbesondere, auf nicht *kompatible* Messungen zu gründen, die auf tatsächlicher Hardware nicht möglich wären.</span><span class="sxs-lookup"><span data-stu-id="f9118-140">In particular, this allows us to reason about *incompatible* measurements that would be impossible on actual hardware.</span></span>

<span data-ttu-id="f9118-141">Angenommen, `P : Qubit => Unit` Es handelt sich um einen Vorgang, der für die Vorbereitung des Zustands $ \ket{\psi} $ vorgesehen ist, wenn seine Eingabe im Status $ \ket {0} $ liegt.</span><span class="sxs-lookup"><span data-stu-id="f9118-141">Suppose that `P : Qubit => Unit` is an operation intended to prepare the state $\ket{\psi}$ when its input is in the state $\ket{0}$.</span></span>
<span data-ttu-id="f9118-142">Let $ \ket{\psi '} $ ist der tatsächliche Zustand, der von vorbereitet wird `P` .</span><span class="sxs-lookup"><span data-stu-id="f9118-142">Let $\ket{\psi'}$ be the actual state prepared by `P`.</span></span>
<span data-ttu-id="f9118-143">Dann gibt $ \ket{\psi} = \ket{\psi '} $ nur dann zurück, wenn $ \ket{\psi '} $ in der durch $ \ket{\psi} $ beschriebenen Achse gemessen wird `Zero` .</span><span class="sxs-lookup"><span data-stu-id="f9118-143">Then, $\ket{\psi} = \ket{\psi'}$ if and only if measuring $\ket{\psi'}$ in the axis described by $\ket{\psi}$ always returns `Zero`.</span></span>
<span data-ttu-id="f9118-144">Das heißt: \begin{align} \ket{\psi} = \ket{\psi '} \text{if und only if} \braket{\psi | \psi '} = 1.</span><span class="sxs-lookup"><span data-stu-id="f9118-144">That is, \begin{align} \ket{\psi} = \ket{\psi'} \text{ if and only if } \braket{\psi | \psi'} = 1.</span></span>
<span data-ttu-id="f9118-145">\end{align} mit den primitiven Vorgängen, die in der Einleitung definiert sind, können wir direkt eine Messung ausführen, die zurückgibt, `Zero` Wenn $ \ket{\psi} $ ein eigen Zustand eines der Pauli-Operatoren ist.</span><span class="sxs-lookup"><span data-stu-id="f9118-145">\end{align} Using the primitive operations defined in the prelude, we can directly perform a measurement that returns `Zero` if $\ket{\psi}$ is an eigenstate of one of the Pauli operators.</span></span>


<span data-ttu-id="f9118-146">Der Vorgang <xref:microsoft.quantum.diagnostics.assertqubit> bietet eine besonders hilfreiche kurznote, um dies zu tun, wenn wir die Assertionen $ \ket{\psi} = \ket $ testen möchten {0} .</span><span class="sxs-lookup"><span data-stu-id="f9118-146">The operation <xref:microsoft.quantum.diagnostics.assertqubit> provides a particularly useful shorthand to do so in the case that we wish to test the assertion $\ket{\psi} = \ket{0}$.</span></span>
<span data-ttu-id="f9118-147">Dies ist beispielsweise häufig der Fall, wenn die Berechnung von Ancilla Qubits an $ \ket $ vor der Freigabe nicht berechnet wurde {0} .</span><span class="sxs-lookup"><span data-stu-id="f9118-147">This is common, for instance, when we have uncomputed to return ancilla qubits to $\ket{0}$ before releasing them.</span></span>
<span data-ttu-id="f9118-148">Die Bestätigung von $ \ket {0} $ ist auch hilfreich, wenn wir bestätigen möchten, dass zwei Zustands Vorbereitung `P` und- `Q` Vorgänge jeweils denselben Status vorbereiten und wenn von `Q` unterstützt wird `Adjoint` .</span><span class="sxs-lookup"><span data-stu-id="f9118-148">Asserting against $\ket{0}$ is also useful when we wish to assert that two state preparation `P` and `Q` operations both prepare the same state, and when `Q` supports `Adjoint`.</span></span>
<span data-ttu-id="f9118-149">Insbesondere</span><span class="sxs-lookup"><span data-stu-id="f9118-149">In particular,</span></span>

```qsharp
using (register = Qubit()) {
    P(register);
    Adjoint Q(register);

    AssertQubit(Zero, register);
}
```

<span data-ttu-id="f9118-150">Im Allgemeinen haben wir jedoch möglicherweise keinen Zugriff auf Assertionen über Zustände, die nicht mit den eigen Zuständen von Pauli-Operatoren übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="f9118-150">More generally, however, we may not have access to assertions about states that do not coincide with eigenstates of Pauli operators.</span></span>
<span data-ttu-id="f9118-151">Beispielsweise ist $ \ket{\psi} = (\ket {0} + e ^ {i \pi/8} \ket {1} )/\sqrt {2} $ kein eigen Zustand eines Pauli-Operators, sodass wir nicht verwenden können, <xref:microsoft.quantum.diagnostics.assertmeasurementprobability> um eindeutig zu ermitteln, ob der Status $ \ket{\psi '} $ gleich $ \ket{\psi} $ ist.</span><span class="sxs-lookup"><span data-stu-id="f9118-151">For example, $\ket{\psi} = (\ket{0} + e^{i \pi / 8} \ket{1}) / \sqrt{2}$ is not an eigenstate of any Pauli operator, such that we cannot use <xref:microsoft.quantum.diagnostics.assertmeasurementprobability> to uniquely determine that a state $\ket{\psi'}$ is equal to $\ket{\psi}$.</span></span>
<span data-ttu-id="f9118-152">Stattdessen müssen wir die Assert-Assertionen $ \ket{\psi '} = \ket{\psi} $ in Annahmen zerlegen, die direkt mit den primitiven getestet werden können, die von unserem Simulator unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="f9118-152">Instead, we must decompose the assertion $\ket{\psi'} = \ket{\psi}$ into assumptions that can be directly tested using  the primitives supported by our simulator.</span></span>
<span data-ttu-id="f9118-153">Verwenden Sie hierzu $ \ket{\psi} = \alpha \ket {0} + \beta \ket {1} $ für die komplexen Zahlen $ \alpha = a \_ r + a \_ i i $ und $ \beta $.</span><span class="sxs-lookup"><span data-stu-id="f9118-153">To do so, let $\ket{\psi} = \alpha \ket{0} + \beta \ket{1}$ for complex numbers $\alpha = a\_r + a\_i i$ and $\beta$.</span></span>
<span data-ttu-id="f9118-154">Beachten Sie, dass für diesen Ausdruck vier reelle Zahlen ($ \{ a \_ r), a \_ i, b \_ r, b \_ i \} $ zur Angabe erforderlich sind, da jede komplexe Zahl als Summe eines reellen und imaginären Teils ausgedrückt werden kann.</span><span class="sxs-lookup"><span data-stu-id="f9118-154">Note that this expression requires four real numbers $\{a\_r, a\_i, b\_r, b\_i\}$ to specify, as each complex number can be expressed as the sum of a real and imaginary part.</span></span>
<span data-ttu-id="f9118-155">Aufgrund der globalen Phase können Sie jedoch $a \_ i = $0 auswählen, sodass nur drei reelle Zahlen erforderlich sind, um einen Single-Qubit-Zustand eindeutig anzugeben.</span><span class="sxs-lookup"><span data-stu-id="f9118-155">Due to the global phase, however, we can choose $a\_i = 0$, such that we only need three real numbers to uniquely specify a single-qubit state.</span></span>

<span data-ttu-id="f9118-156">Daher müssen wir drei Assertionen angeben, die voneinander unabhängig sind, um den erwarteten Status zu bestätigen.</span><span class="sxs-lookup"><span data-stu-id="f9118-156">Thus, we need to specify three assertions which are independent of each other in order to assert the state that we expect.</span></span>
<span data-ttu-id="f9118-157">Hierzu finden Sie die Wahrscheinlichkeit `Zero` , dass die einzelnen Pauli-Messungen für "$ \alpha $" und "$ \beta $" beachtet werden, und die einzelnen Ansprüche unabhängig voneinander zu bestätigen.</span><span class="sxs-lookup"><span data-stu-id="f9118-157">We do so by finding the probability of observing `Zero` for each Pauli measurement given $\alpha$ and $\beta$, and asserting each independently.</span></span>
<span data-ttu-id="f9118-158">Lassen Sie $x $, $y $ und $z $ be- `Result` Werte für Pauli $X $, $Y $, bzw. $Z $-Messungen aus.</span><span class="sxs-lookup"><span data-stu-id="f9118-158">Let $x$, $y$, and $z$ be `Result` values for Pauli $X$, $Y$, and $Z$ measurements respectively.</span></span>
<span data-ttu-id="f9118-159">Verwenden Sie dann die Wahrscheinlichkeitsfunktion für Quantum-Messungen, \begin{align} \pr (x = \texttt{Zero} | \alpha, \beta) & = \bruchteil 12 + a \_ r b \_ r + a \_ i b \_ i \\ \\ \pr (y = \texttt{Zero} | \alpha, \beta) & = \bruchteil 12 + a \_ r b \_ i-a \_ i b \_ r \\ \\ \pr (z = \texttt{Zero} | \alpha, \beta) & = \bruch12\left (1 + a \_ r ^ 2 + a \_ i ^ 2 + b \_ r ^ 2 + b \_ i ^ 2 \right).</span><span class="sxs-lookup"><span data-stu-id="f9118-159">Then, using the likelihood function for quantum measurements, \begin{align} \Pr(x = \texttt{Zero} | \alpha, \beta) & = \frac12 + a\_r b\_r + a\_i b\_i \\\\ \Pr(y = \texttt{Zero} | \alpha, \beta) & = \frac12 + a\_r b\_i - a\_i b\_r \\\\ \Pr(z = \texttt{Zero} | \alpha, \beta) & = \frac12\left( 1 + a\_r^2 + a\_i^2 + b\_r^2 + b\_i^2 \right).</span></span>
<span data-ttu-id="f9118-160">\end{align}</span><span class="sxs-lookup"><span data-stu-id="f9118-160">\end{align}</span></span>

<span data-ttu-id="f9118-161">Der- <xref:microsoft.quantum.diagnostics.assertqubitisinstatewithintolerance> Vorgang implementiert diese Assertionen anhand von Darstellungen von $ \alpha $ und $ \beta $ als Werte des Typs <xref:microsoft.quantum.math.complex> .</span><span class="sxs-lookup"><span data-stu-id="f9118-161">The <xref:microsoft.quantum.diagnostics.assertqubitisinstatewithintolerance> operation implements these assertions given representations of $\alpha$ and $\beta$ as values of type <xref:microsoft.quantum.math.complex>.</span></span>
<span data-ttu-id="f9118-162">Dies ist hilfreich, wenn der erwartete Zustand mathematisch berechnet werden kann.</span><span class="sxs-lookup"><span data-stu-id="f9118-162">This is helpful when the expected state can be computed mathematically.</span></span>

### <a name="asserting-equality-of-quantum-operations"></a><span data-ttu-id="f9118-163">Assert-Gleichheit von Quantum-Vorgängen</span><span class="sxs-lookup"><span data-stu-id="f9118-163">Asserting Equality of Quantum Operations</span></span> ###

<span data-ttu-id="f9118-164">Bisher haben wir uns mit Test Vorgängen beschäftigt, bei denen bestimmte Zustände vorbereitet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f9118-164">Thus far, we have been concerned with testing operations which are intended to prepare particular states.</span></span>
<span data-ttu-id="f9118-165">Häufig ist es jedoch interessant, wie ein Vorgang für willkürliche Eingaben und nicht für eine einzelne, behobene Eingabe agiert.</span><span class="sxs-lookup"><span data-stu-id="f9118-165">Often, however, we are interested in how an operation acts for arbitrary inputs rather than for a single fixed input.</span></span>
<span data-ttu-id="f9118-166">Angenommen, wir haben einen Vorgang implementiert, `U : ((Double, Qubit[]) => () : Adjoint)` der einer Familie einheitlicher Operatoren $U (t) $ entspricht, und haben einen expliziten Block bereitgestellt, `adjoint` anstatt zu verwenden `adjoint auto` .</span><span class="sxs-lookup"><span data-stu-id="f9118-166">For example, suppose we have implemented an operation `U : ((Double, Qubit[]) => () : Adjoint)` corresponding to a family of unitary operators $U(t)$, and have provided an explicit `adjoint` block instead of using `adjoint auto`.</span></span>
<span data-ttu-id="f9118-167">Wir sind vielleicht daran interessiert, dass $U ^ \dagger (t) = U (-t) $, wie erwartet, wenn $t $ eine Entwicklungszeit darstellt.</span><span class="sxs-lookup"><span data-stu-id="f9118-167">We may be interested in asserting that $U^\dagger(t) = U(-t)$, as expected if $t$ represents an evolution time.</span></span>

<span data-ttu-id="f9118-168">Im Allgemeinen gibt es zwei verschiedene Strategien, die Sie befolgen können, um die-Assertionen für zwei Vorgänge durchführen `U` und `V` identisch agieren.</span><span class="sxs-lookup"><span data-stu-id="f9118-168">Broadly speaking, there are two different strategies that we can follow in making the assertion that two operations `U` and `V` act identically.</span></span>
<span data-ttu-id="f9118-169">Zuerst können wir überprüfen, ob `U(target); (Adjoint V)(target);` jeden Status in einer bestimmten Weise beibehält.</span><span class="sxs-lookup"><span data-stu-id="f9118-169">First, we can check that `U(target); (Adjoint V)(target);` preserves each state in a given basis.</span></span>
<span data-ttu-id="f9118-170">Zum anderen können wir überprüfen, ob die-Funktion `U(target); (Adjoint V)(target);` bei der Hälfte eines entzweitigen Zustands diese entanglement beibehält.</span><span class="sxs-lookup"><span data-stu-id="f9118-170">Second, we can check that `U(target); (Adjoint V)(target);` acting on half of an entangled state preserves that entanglement.</span></span>
<span data-ttu-id="f9118-171">Diese Strategien werden von den Canon <xref:microsoft.quantum.diagnostics.assertoperationsequalinplace> -Vorgängen <xref:microsoft.quantum.diagnostics.assertoperationsequalreferenced> bzw. implementiert.</span><span class="sxs-lookup"><span data-stu-id="f9118-171">These strategies are implemented by the canon operations <xref:microsoft.quantum.diagnostics.assertoperationsequalinplace> and <xref:microsoft.quantum.diagnostics.assertoperationsequalreferenced>, respectively.</span></span>

> [!NOTE]
> <span data-ttu-id="f9118-172">Die oben beschriebene referenzierte-Assertionen basiert auf dem [' Choi – jamiłkowski '-"isomorphism](https://en.wikipedia.org/wiki/Channel-state_duality)", einem mathematischen Framework, das Vorgänge auf $n $ Qubits mit entbickten Zuständen in $2N $ Qubits verknüpft.</span><span class="sxs-lookup"><span data-stu-id="f9118-172">The referenced assertion discussed above works based on the [Choi–Jamiłkowski isomorphism](https://en.wikipedia.org/wiki/Channel-state_duality), a mathematical framework which relates operations on $n$ qubits to entangled states on $2n$ qubits.</span></span>
> <span data-ttu-id="f9118-173">Insbesondere wird der Identitäts Vorgang für $n $ Qubits durch $n $ Kopien des entspitzen Zustands $ \ket{\ beta_ {00} } \mathrel{: =} (\ket {00} + \ket {11} )/\sqrt {2} $ dargestellt.</span><span class="sxs-lookup"><span data-stu-id="f9118-173">In particular, the identity operation on $n$ qubits is represented by $n$ copies of the entangled state $\ket{\beta_{00}} \mathrel{:=} (\ket{00} + \ket{11}) / \sqrt{2}$.</span></span>
> <span data-ttu-id="f9118-174">Der Vorgang <xref:microsoft.quantum.preparation.preparechoistate> implementiert dieses "isomorphism" und bereitet einen Zustand vor, der einen bestimmten Vorgang darstellt.</span><span class="sxs-lookup"><span data-stu-id="f9118-174">The operation <xref:microsoft.quantum.preparation.preparechoistate> implements this isomorphism, preparing a state that represents a given operation.</span></span>

<span data-ttu-id="f9118-175">Diese Strategien werden ungefähr durch einen Zeit-–-Bereich unterschieden.</span><span class="sxs-lookup"><span data-stu-id="f9118-175">Roughly, these strategies are distinguished by a time–space tradeoff.</span></span>
<span data-ttu-id="f9118-176">Das Durchlaufen der einzelnen Eingabe Zustände erfordert zusätzliche Zeit, während für die Verwendung von jede Verflechtungen als Verweis zusätzliche Qubits gespeichert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="f9118-176">Iterating through each input state takes additional time, while using entanglement as a reference requires storing additional qubits.</span></span>
<span data-ttu-id="f9118-177">In Fällen, in denen ein Vorgang einen umkehrbaren klassischen Vorgang implementiert, sodass wir nur an seinem Verhalten hinsichtlich der Berechnungsbasis Zustände interessiert sind, <xref:microsoft.quantum.diagnostics.assertoperationsequalinplacecompbasis> testet die Gleichheit dieser eingeschränkten Eingaben.</span><span class="sxs-lookup"><span data-stu-id="f9118-177">In cases where an operation implements a reversible classical operation, such that we are only interested in its behavior on computational basis states, <xref:microsoft.quantum.diagnostics.assertoperationsequalinplacecompbasis> tests equality on this restricted set of inputs.</span></span>

> [!TIP]
> <span data-ttu-id="f9118-178">Die Iteration von Eingabe Zuständen wird von den enumerationsvorgängen <xref:microsoft.quantum.canon.iteratethroughcartesianproduct> und behandelt <xref:microsoft.quantum.canon.iteratethroughcartesianpower> .</span><span class="sxs-lookup"><span data-stu-id="f9118-178">The iteration over input states is handled by the enumeration operations <xref:microsoft.quantum.canon.iteratethroughcartesianproduct> and <xref:microsoft.quantum.canon.iteratethroughcartesianpower>.</span></span>
> <span data-ttu-id="f9118-179">Diese Vorgänge sind in der Regel für das Anwenden eines Vorgangs auf jedes Element des kartesischen Produkts zwischen zwei oder mehr Sätzen nützlich.</span><span class="sxs-lookup"><span data-stu-id="f9118-179">These operations are useful more generally for applying an operation to each element of the Cartesian product between two or more sets.</span></span>

<span data-ttu-id="f9118-180">Kritischer ist jedoch, dass in den beiden Ansätzen verschiedene Eigenschaften der Vorgänge überprüft werden, die überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="f9118-180">More critically, however, the two approaches test different properties of the operations under examination.</span></span>
<span data-ttu-id="f9118-181">Da die direkte-Assertionen jeden Vorgang mehrmals aufruft, können sich alle zufälligen Optionen und Messergebnisse zwischen den Aufrufen jeweils einmal für jeden Eingabe Status ändern.</span><span class="sxs-lookup"><span data-stu-id="f9118-181">Since the in-place assertion calls each operation multiple times, once for each input state, any random choices and measurement results might change between calls.</span></span>
<span data-ttu-id="f9118-182">Im Gegensatz dazu wird jeder Vorgang von der referenzierten-Assertionen genau einmal aufgerufen, sodass überprüft wird, ob die Vorgänge *in einem einzelnen Screenshot*gleich sind.</span><span class="sxs-lookup"><span data-stu-id="f9118-182">By contrast, the referenced assertion calls each operation exactly once, such that it checks that the operations are equal *in a single shot*.</span></span>
<span data-ttu-id="f9118-183">Beide Tests sind nützlich, um die Richtigkeit von Quantum-Programmen sicherzustellen.</span><span class="sxs-lookup"><span data-stu-id="f9118-183">Both of these tests are useful in ensuring the correctness of quantum programs.</span></span>


## <a name="further-reading"></a><span data-ttu-id="f9118-184">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="f9118-184">Further Reading</span></span> ##

- <xref:microsoft.quantum.guide.testingdebugging>
- <xref:microsoft.quantum.diagnostics>