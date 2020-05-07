---
title: 'F #-Techniken-alles vereinen'
description: 'Gehen Sie durch ein einfaches Q #-Programm, das die Quantum-Teleportation veranschaulicht.'
uid: microsoft.quantum.techniques.puttingittogether
author: QuantumWriter
ms.author: Christopher.Granade@microsoft.com
ms.date: 12/11/2017
ms.topic: article
ms.openlocfilehash: 4bd91699017e4c1acd9f4449b8a65e39bd07878e
ms.sourcegitcommit: b6b8459eb654040f1e19f66411b29fc9e48e95c9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2020
ms.locfileid: "82030564"
---
# <a name="putting-it-all-together-teleportation"></a><span data-ttu-id="fdd97-103">Alles zusammen: teleportierung</span><span class="sxs-lookup"><span data-stu-id="fdd97-103">Putting It All Together: Teleportation</span></span> #
<span data-ttu-id="fdd97-104">Wir kehren zum Beispiel der in [Quantum](xref:microsoft.quantum.concepts.circuits)-Leitungen definierten Teleportations-Verbindung zurück.</span><span class="sxs-lookup"><span data-stu-id="fdd97-104">Let's return to the example of the teleportation circuit defined in [Quantum Circuits](xref:microsoft.quantum.concepts.circuits).</span></span> <span data-ttu-id="fdd97-105">Wir werden diese Informationen verwenden, um die bisher gelernten Konzepte zu veranschaulichen.</span><span class="sxs-lookup"><span data-stu-id="fdd97-105">We're going to use this to illustrate the concepts we've learned so far.</span></span> <span data-ttu-id="fdd97-106">Eine Erläuterung der Quantum-Teleportation finden Sie unten für Personen, die mit der Theorie nicht vertraut sind, gefolgt von einer exemplarischen Vorgehensweise der Code Implementierung in f #.</span><span class="sxs-lookup"><span data-stu-id="fdd97-106">An explanation of quantum teleportation is provided below for those who are unfamiliar with the theory, followed by a walkthrough of the code implementation in Q#.</span></span> 

## <a name="quantum-teleportation-theory"></a><span data-ttu-id="fdd97-107">Quantum-Teleportation: Theorie</span><span class="sxs-lookup"><span data-stu-id="fdd97-107">Quantum Teleportation: Theory</span></span>
<span data-ttu-id="fdd97-108">Die Quantum-Teleportation ist eine Technik zum Senden eines unbekannten Quantums (als "__Message__" bezeichnet) von einem Qubit an einem Speicherort an einem Ort an einem Qubit an einem anderen Speicherort (wir bezeichnen diese Qubits als __"This" bzw__. "__there__").</span><span class="sxs-lookup"><span data-stu-id="fdd97-108">Quantum teleportation is a technique for sending an unknown quantum state (which we'll refer to as the '__message__') from a qubit in one location to a qubit in another location (we'll refer to these qubits as '__here__' and '__there__', respectively).</span></span> <span data-ttu-id="fdd97-109">Wir können unsere __Nachricht__ mithilfe der Dirac-Notation als Vektor darstellen:</span><span class="sxs-lookup"><span data-stu-id="fdd97-109">We can represent our __message__ as a vector using Dirac notation:</span></span> 

<span data-ttu-id="fdd97-110">$ $ \ket{\psi} = \alpha\ket{0} + \beta\ket{1} $ $</span><span class="sxs-lookup"><span data-stu-id="fdd97-110">$$ \ket{\psi} = \alpha\ket{0} + \beta\ket{1} $$</span></span>

<span data-ttu-id="fdd97-111">Der Status des __nachrichtenqubits__ ist für uns unbekannt, da wir die Werte von $ \alpha $ und $ \beta $ nicht kennen.</span><span class="sxs-lookup"><span data-stu-id="fdd97-111">The __message__ qubit's state is unknown to us as we do not know the values of $\alpha$ and $\beta$.</span></span>

### <a name="step-1-create-an-entangled-state"></a><span data-ttu-id="fdd97-112">Schritt 1: Erstellen eines entkoppelt-Zustands</span><span class="sxs-lookup"><span data-stu-id="fdd97-112">Step 1: Create an entangled state</span></span>
<span data-ttu-id="fdd97-113">Um die __Nachricht__ zu senden, muss das Qubit __hier__ mit dem Qubit entkoppelt __werden.__</span><span class="sxs-lookup"><span data-stu-id="fdd97-113">In order to send the __message__ we need for the qubit __here__ to be entangled with the qubit __there__.</span></span> <span data-ttu-id="fdd97-114">Dies wird erreicht, indem ein Hadamard-Gate, gefolgt von einem CNOT-Gate, angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="fdd97-114">This is achieved by applying a Hadamard gate, followed by a CNOT gate.</span></span> <span data-ttu-id="fdd97-115">Sehen wir uns die mathematische hinter diesen Gate-Vorgängen an.</span><span class="sxs-lookup"><span data-stu-id="fdd97-115">Let's look at the math behind these gate operations.</span></span>

<span data-ttu-id="fdd97-116">Wir beginnen mit den __Qubits und__ __dort__ sowohl im $ \ket{0}$-Zustand.</span><span class="sxs-lookup"><span data-stu-id="fdd97-116">We will begin with the qubits __here__ and __there__ both in the $\ket{0}$ state.</span></span> <span data-ttu-id="fdd97-117">Nachdem Sie diese Qubits entwursten, befinden Sie sich im Zustand:</span><span class="sxs-lookup"><span data-stu-id="fdd97-117">After entangling these qubits, they are in the state:</span></span>

<span data-ttu-id="fdd97-118">$ $ \ket{\phi ^ +} = \frac{1}{\sqrt{2}} (\ket{00} + \ket{11}) $ $</span><span class="sxs-lookup"><span data-stu-id="fdd97-118">$$ \ket{\phi^+} = \frac{1}{\sqrt{2}}(\ket{00} + \ket{11}) $$</span></span>

### <a name="step-2-send-the-message"></a><span data-ttu-id="fdd97-119">Schritt 2: Senden der Nachricht</span><span class="sxs-lookup"><span data-stu-id="fdd97-119">Step 2: Send the message</span></span>
<span data-ttu-id="fdd97-120">Zum Senden der __Nachricht__ wenden wir zuerst ein CNOT Gate mit dem __Message__ Qubit und diesem Qubit als Eingaben an (das __Nachrichten__ Qubit ist das Steuerelement, __und das this-Qubit__ ist das __Ziel-__ Qubit, in diesem Fall).</span><span class="sxs-lookup"><span data-stu-id="fdd97-120">To send the __message__ we first apply a CNOT gate with the __message__ qubit and __here__ qubit as inputs (the __message__ qubit being the control and the __here__ qubit being the target qubit, in this instance).</span></span> <span data-ttu-id="fdd97-121">Dieser Eingabe Zustand kann geschrieben werden:</span><span class="sxs-lookup"><span data-stu-id="fdd97-121">This input state can be written:</span></span>

<span data-ttu-id="fdd97-122">$ $ \ket{\psi}\ket{\phi ^ +} = (\alpha\ket{0} + \beta\ket{1}) (\frac{1}{\sqrt{2}} (\ket{00} + \ket{11})) $ $</span><span class="sxs-lookup"><span data-stu-id="fdd97-122">$$ \ket{\psi}\ket{\phi^+} = (\alpha\ket{0} + \beta\ket{1})(\frac{1}{\sqrt{2}}(\ket{00} + \ket{11})) $$</span></span>

<span data-ttu-id="fdd97-123">Dies erweitert zu:</span><span class="sxs-lookup"><span data-stu-id="fdd97-123">This expands to:</span></span>

<span data-ttu-id="fdd97-124">$ $ \ket{\psi}\ket{\phi ^ +} = \frac{\alpha}{\sqrt{2}} \ket{000} + \frac{\alpha}{\sqrt{2}} \ket{011} + \frac{\beta}{\sqrt{2}} \ket{100} + \frac{\beta}{\sqrt{2}} \ket{111} $ $</span><span class="sxs-lookup"><span data-stu-id="fdd97-124">$$ \ket{\psi}\ket{\phi^+} = \frac{\alpha}{\sqrt{2}}\ket{000} + \frac{\alpha}{\sqrt{2}}\ket{011} + \frac{\beta}{\sqrt{2}}\ket{100} + \frac{\beta}{\sqrt{2}}\ket{111} $$</span></span>

<span data-ttu-id="fdd97-125">Zur Erinnerung: das CNOT-Gate flippt das Ziel-Qubit, wenn das Steuerelement-Qubit 1 ist.</span><span class="sxs-lookup"><span data-stu-id="fdd97-125">As a reminder, the CNOT gate flips the target qubit when the control qubit is 1.</span></span> <span data-ttu-id="fdd97-126">Eine Eingabe von $ \ket{000}$ führt z. b. zu keiner Änderung, da das erste Qubit (das Steuerelement) 0 (null) ist.</span><span class="sxs-lookup"><span data-stu-id="fdd97-126">So for example, an input of $\ket{000}$ will result in no change as the first qubit (the control) is 0.</span></span> <span data-ttu-id="fdd97-127">Nehmen Sie jedoch einen Fall, bei dem das erste Qubit 1 ist, z. b. eine Eingabe{100}von $ \ket $.</span><span class="sxs-lookup"><span data-stu-id="fdd97-127">However, take a case where the first qubit is 1 - for example an input of $\ket{100}$.</span></span> <span data-ttu-id="fdd97-128">In diesem Beispiel ist die Ausgabe $ \ket{110}$, da das zweite Qubit (das Ziel) vom CNOT-Gate gekippt wird.</span><span class="sxs-lookup"><span data-stu-id="fdd97-128">In this instance, the output is $\ket{110}$ as the second qubit (the target) is flipped by the CNOT gate.</span></span>

<span data-ttu-id="fdd97-129">Sehen wir uns nun unsere Ausgabe an, sobald das CNOT-Gate in der obigen Eingabe agiert hat.</span><span class="sxs-lookup"><span data-stu-id="fdd97-129">Let's now consider our output once the CNOT gate has acted on our input above.</span></span> <span data-ttu-id="fdd97-130">Es wird folgendes Ergebnis ausgegeben:</span><span class="sxs-lookup"><span data-stu-id="fdd97-130">The result is:</span></span>

<span data-ttu-id="fdd97-131">$ $ \frac{\alpha}{\sqrt{2}} \ket{000} + \frac{\alpha}{\sqrt{2}} \ket{011} + \frac{\beta}{\sqrt{2}} \ket{110} + \frac{\beta}{\sqrt{2}} \ket{101} $ $</span><span class="sxs-lookup"><span data-stu-id="fdd97-131">$$ \frac{\alpha}{\sqrt{2}}\ket{000} + \frac{\alpha}{\sqrt{2}}\ket{011} + \frac{\beta}{\sqrt{2}}\ket{110} + \frac{\beta}{\sqrt{2}}\ket{101} $$</span></span>

<span data-ttu-id="fdd97-132">Der nächste Schritt zum Senden der __Nachricht__ ist das Anwenden eines Hadamard-Gates auf das __Message__ -Qubit (das die erste Qubit jedes Begriffs ist).</span><span class="sxs-lookup"><span data-stu-id="fdd97-132">The next step to send the __message__ is to apply a Hadamard gate to the __message__ qubit (that's the first qubit of each term).</span></span> 

<span data-ttu-id="fdd97-133">Zur Erinnerung: das Hadamard-Gate führt Folgendes aus:</span><span class="sxs-lookup"><span data-stu-id="fdd97-133">As a reminder, the Hadamard gate does the following:</span></span>

<span data-ttu-id="fdd97-134">Eingabe</span><span class="sxs-lookup"><span data-stu-id="fdd97-134">Input</span></span> | <span data-ttu-id="fdd97-135">Output</span><span class="sxs-lookup"><span data-stu-id="fdd97-135">Output</span></span>
---------------------------| ---------------------------------------------------------------
<span data-ttu-id="fdd97-136">$ \ket{0}$</span><span class="sxs-lookup"><span data-stu-id="fdd97-136">$\ket{0}$</span></span>  | <span data-ttu-id="fdd97-137">$ \frac{1}{\sqrt{2}} (\ket{0} + \ket{1}) $</span><span class="sxs-lookup"><span data-stu-id="fdd97-137">$\frac{1}{\sqrt{2}}(\ket{0} + \ket{1})$</span></span>
<span data-ttu-id="fdd97-138">$ \ket{1}$</span><span class="sxs-lookup"><span data-stu-id="fdd97-138">$\ket{1}$</span></span>  | <span data-ttu-id="fdd97-139">$ \frac{1}{\sqrt{2}} (\ket{0} -\ket{1}) $</span><span class="sxs-lookup"><span data-stu-id="fdd97-139">$\frac{1}{\sqrt{2}}(\ket{0} - \ket{1})$</span></span>

<span data-ttu-id="fdd97-140">Wenn wir das Hadamard-Gate auf das erste Qubit für jeden Begriff der obigen Ausgabe anwenden, erhalten wir folgendes Ergebnis:</span><span class="sxs-lookup"><span data-stu-id="fdd97-140">If we apply the Hadamard gate to the first qubit of each term of our output above, we get the following result:</span></span>

<span data-ttu-id="fdd97-141">$ $ \frac{\alpha}{\sqrt{2}} (\frac{1}{\sqrt{2}} (\ket{0} + \ket{1})) \ket{00} + \frac{\alpha}{\sqrt{2}} (\frac{1}{\sqrt{2}} (\ket{0} + \ket{1})) \ket{11} + \frac{\beta}{\sqrt{2}} (\frac{1}{\sqrt{2}} (\ket{0} -\ket{1})) \ket{10} + \frac{\beta}{\sqrt{2}} (\frac{1}{\sqrt{2}} (\ket{0} -\ket{1})) \ket{01} $ $</span><span class="sxs-lookup"><span data-stu-id="fdd97-141">$$ \frac{\alpha}{\sqrt{2}}(\frac{1}{\sqrt{2}}(\ket{0} + \ket{1}))\ket{00} + \frac{\alpha}{\sqrt{2}}(\frac{1}{\sqrt{2}}(\ket{0} + \ket{1}))\ket{11} + \frac{\beta}{\sqrt{2}}(\frac{1}{\sqrt{2}}(\ket{0} - \ket{1}))\ket{10} + \frac{\beta}{\sqrt{2}}(\frac{1}{\sqrt{2}}(\ket{0} - \ket{1}))\ket{01} $$</span></span>

<span data-ttu-id="fdd97-142">Beachten Sie, dass jeder Begriff $2 \frac{1}{\sqrt{2}} $ Factors hat.</span><span class="sxs-lookup"><span data-stu-id="fdd97-142">Note that each term has two $\frac{1}{\sqrt{2}}$ factors.</span></span> <span data-ttu-id="fdd97-143">Wir können diese multiplizieren, indem wir folgendes Ergebnis erhalten:</span><span class="sxs-lookup"><span data-stu-id="fdd97-143">We can multiply these out giving the following result:</span></span>

<span data-ttu-id="fdd97-144">$ $ \bruchteil {\alpha}{2}(\ket{0} + \ket{1}) \ket{00} + \bruch {\alpha}{2}(\ket{0} + \ket{1}) \ket{11} + \bruch {\beta}{2}(\ket{0} -\ket{1}) \ket{10} + \bruch {\beta}{2}(\ket{0} -\ket{1}) \ket{01} $ $</span><span class="sxs-lookup"><span data-stu-id="fdd97-144">$$ \frac{\alpha}{2}(\ket{0} + \ket{1})\ket{00} + \frac{\alpha}{2}(\ket{0} + \ket{1})\ket{11} + \frac{\beta}{2}(\ket{0} - \ket{1})\ket{10} + \frac{\beta}{2}(\ket{0} - \ket{1})\ket{01} $$</span></span>

<span data-ttu-id="fdd97-145">"$ \Frac{1}{2}$ Factor" ist für jeden Begriff üblich, sodass wir ihn jetzt außerhalb der Klammern nehmen können:</span><span class="sxs-lookup"><span data-stu-id="fdd97-145">The  $\frac{1}{2}$ factor is common to each term so we can now take it outside the brackets:</span></span>

<span data-ttu-id="fdd97-146">$ $ \frac{1}{2}\big [\alpha (\ket{0} + \ket{1}) \ket{00} + \alpha (\ket{0} + \ket{1}) \ket{11} + \beta (\ket{0} -\ket{1}) \ket{10} + \beta (\ket{0} -\ket{1}) \ket{01}\big] $ $</span><span class="sxs-lookup"><span data-stu-id="fdd97-146">$$ \frac{1}{2}\big[\alpha(\ket{0} + \ket{1})\ket{00} + \alpha(\ket{0} + \ket{1})\ket{11} + \beta(\ket{0} - \ket{1})\ket{10} + \beta(\ket{0} - \ket{1})\ket{01}\big] $$</span></span>

<span data-ttu-id="fdd97-147">Anschließend können wir die Klammern für jeden Begriff multiplizieren, der Folgendes bietet:</span><span class="sxs-lookup"><span data-stu-id="fdd97-147">We can then multiply out the brackets for each term giving:</span></span>

<span data-ttu-id="fdd97-148">$ $ \frac{1}{2}\big [\alpha\ket{000} + \alpha\ket{100} + \alpha\ket{011} + \alpha\ket{111} + \beta\ket{010} -\beta\ket{110} + \beta\ket{001} -\beta\ket{101}\big] $ $</span><span class="sxs-lookup"><span data-stu-id="fdd97-148">$$ \frac{1}{2}\big[\alpha\ket{000} + \alpha\ket{100} + \alpha\ket{011} + \alpha\ket{111} + \beta\ket{010} - \beta\ket{110} + \beta\ket{001} - \beta\ket{101}\big] $$</span></span>

### <a name="step-3-measure-the-result"></a><span data-ttu-id="fdd97-149">Schritt 3: Messen des Ergebnisses</span><span class="sxs-lookup"><span data-stu-id="fdd97-149">Step 3: Measure the result</span></span>

<span data-ttu-id="fdd97-150">Da __hier__ __und die entkoppelt werden,__ wirkt sich jede Messung __hier__ auf den Status von __dort__aus.</span><span class="sxs-lookup"><span data-stu-id="fdd97-150">Due to __here__ and __there__ being entangled, any measurement on __here__ will affect the state of __there__.</span></span> <span data-ttu-id="fdd97-151">Wenn wir das erste und zweite Qubit (__Nachricht__ und __hier__) messen, können wir aufgrund dieser Eigenschaft von entanglement erfahren, welcher Zustand in __vorhanden__ ist.</span><span class="sxs-lookup"><span data-stu-id="fdd97-151">If we measure the first and second qubit (__message__ and __here__) we can learn what state __there__ is in, due to this property of entanglement.</span></span> 

* <span data-ttu-id="fdd97-152">Wenn wir ein Ergebnis 00 Messen und erzielen, wird die Superposition reduziert, sodass nur die Begriffe mit diesem Ergebnis konsistent sind.</span><span class="sxs-lookup"><span data-stu-id="fdd97-152">If we measure and get a result 00, the superposition collapses, leaving only terms consistent with this result.</span></span> <span data-ttu-id="fdd97-153">Das ist "$ \alpha\ket{000} + \beta\ket{001}$".</span><span class="sxs-lookup"><span data-stu-id="fdd97-153">That's $\alpha\ket{000} +\beta\ket{001}$.</span></span> <span data-ttu-id="fdd97-154">Dies kann mit "$ \ket{00}" (\alpha\ket{0} + \beta\ket{1}) "$" umgestaltet werden.</span><span class="sxs-lookup"><span data-stu-id="fdd97-154">This can be refactored to $\ket{00}(\alpha\ket{0} +\beta\ket{1})$.</span></span> <span data-ttu-id="fdd97-155">Wenn wir also das erste und zweite Qubit mit dem Wert 00 Messen, wissen wir, __dass sich das__dritte Qubit im Status $ (\alpha\ket{0} + \beta\ket{1}) $ befindet.</span><span class="sxs-lookup"><span data-stu-id="fdd97-155">Therefore if we measure the first and second qubit to be 00, we know that the third qubit, __there__, is in the state $(\alpha\ket{0} +\beta\ket{1})$.</span></span>
* <span data-ttu-id="fdd97-156">Wenn wir ein Ergebnis 01 Messen und erhalten, wird die Superposition reduziert, sodass nur die Begriffe mit diesem Ergebnis konsistent sind.</span><span class="sxs-lookup"><span data-stu-id="fdd97-156">If we measure and get a result 01, the superposition collapses, leaving only terms consistent with this result.</span></span> <span data-ttu-id="fdd97-157">Das ist "$ \alpha\ket{011} + \beta\ket{010}$".</span><span class="sxs-lookup"><span data-stu-id="fdd97-157">That's $\alpha\ket{011} +\beta\ket{010}$.</span></span> <span data-ttu-id="fdd97-158">Dies kann mit "$ \ket{01}" (\alpha\ket{1} + \beta\ket{0}) "$" umgestaltet werden.</span><span class="sxs-lookup"><span data-stu-id="fdd97-158">This can be refactored to $\ket{01}(\alpha\ket{1} +\beta\ket{0})$.</span></span> <span data-ttu-id="fdd97-159">Wenn wir also das erste und zweite Qubit als "01" Messen, wissen wir, __dass sich das__dritte Qubit im Zustand "$ (\alpha\ket{1} + \beta\ket{0})" befindet.</span><span class="sxs-lookup"><span data-stu-id="fdd97-159">Therefore if we measure the first and second qubit to be 01, we know that the third qubit, __there__, is in the state $(\alpha\ket{1} +\beta\ket{0})$.</span></span>
* <span data-ttu-id="fdd97-160">Wenn wir das Ergebnis 10 Messen und erzielen, wird die Superposition reduziert, sodass nur die Begriffe mit diesem Ergebnis konsistent sind.</span><span class="sxs-lookup"><span data-stu-id="fdd97-160">If we measure and get a result 10, the superposition collapses, leaving only terms consistent with this result.</span></span> <span data-ttu-id="fdd97-161">Das ist "$ \alpha\ket{100} -\beta\ket{101}$".</span><span class="sxs-lookup"><span data-stu-id="fdd97-161">That's $\alpha\ket{100} -\beta\ket{101}$.</span></span> <span data-ttu-id="fdd97-162">Dies kann auf $ \ket{10}(\alpha\ket{0} -\beta\ket{1}) $ umformatiert werden.</span><span class="sxs-lookup"><span data-stu-id="fdd97-162">This can be refactored to $\ket{10}(\alpha\ket{0} -\beta\ket{1})$.</span></span> <span data-ttu-id="fdd97-163">Wenn wir also das erste und zweite Qubit als 10 Messen, wissen wir, __dass sich das__dritte Qubit in dem Status $ (\alpha\ket{0} -\beta\ket{1}) $ befindet.</span><span class="sxs-lookup"><span data-stu-id="fdd97-163">Therefore if we measure the first and second qubit to be 10, we know that the third qubit, __there__, is in the state $(\alpha\ket{0} -\beta\ket{1})$.</span></span>
* <span data-ttu-id="fdd97-164">Wenn wir das Ergebnis 11 Messen und erzielen, wird die Superposition reduziert, sodass nur die Begriffe mit diesem Ergebnis konsistent sind.</span><span class="sxs-lookup"><span data-stu-id="fdd97-164">If we measure and get a result 11, the superposition collapses, leaving only terms consistent with this result.</span></span> <span data-ttu-id="fdd97-165">Das ist "$ \alpha\ket{111} -\beta\ket{110}$".</span><span class="sxs-lookup"><span data-stu-id="fdd97-165">That's $\alpha\ket{111} -\beta\ket{110}$.</span></span> <span data-ttu-id="fdd97-166">Dies kann auf $ \ket{11}(\alpha\ket{1} -\beta\ket{0}) $ umformatiert werden.</span><span class="sxs-lookup"><span data-stu-id="fdd97-166">This can be refactored to $\ket{11}(\alpha\ket{1} -\beta\ket{0})$.</span></span> <span data-ttu-id="fdd97-167">Wenn wir also das erste und zweite Qubit als 11 Messen, wissen wir, __dass sich das__dritte Qubit in dem Status $ (\alpha\ket{1} -\beta\ket{0}) $ befindet.</span><span class="sxs-lookup"><span data-stu-id="fdd97-167">Therefore if we measure the first and second qubit to be 11, we know that the third qubit, __there__, is in the state $(\alpha\ket{1} -\beta\ket{0})$.</span></span>

### <a name="step-4-interpret-the-result"></a><span data-ttu-id="fdd97-168">Schritt 4: interpretieren des Ergebnisses</span><span class="sxs-lookup"><span data-stu-id="fdd97-168">Step 4: Interpret the result</span></span>

<span data-ttu-id="fdd97-169">Die ursprüngliche __Nachricht__ , die wir senden wollten, lautete als Erinnerung:</span><span class="sxs-lookup"><span data-stu-id="fdd97-169">As a reminder, the original __message__ we wished to send was:</span></span>

<span data-ttu-id="fdd97-170">$ $ \ket{\psi} = \alpha\ket{0} + \beta\ket{1} $ $</span><span class="sxs-lookup"><span data-stu-id="fdd97-170">$$ \ket{\psi} = \alpha\ket{0} + \beta\ket{1} $$</span></span>

<span data-ttu-id="fdd97-171">Wir müssen __das Qubit__ in diesen Zustand bringen, damit der empfangene Zustand der gewünschte Zustand ist.</span><span class="sxs-lookup"><span data-stu-id="fdd97-171">We need to get the __there__ qubit into this state, so that the received state is the one that was intended.</span></span> 

* <span data-ttu-id="fdd97-172">Wenn wir gemessen haben und ein Ergebnis von 00 erhalten haben, __befindet sich das__dritte Qubit im Status $ (\alpha\ket{0} + \beta\ket{1}) $.</span><span class="sxs-lookup"><span data-stu-id="fdd97-172">If we measured and got a result of 00, then the third qubit, __there__, is in the state $(\alpha\ket{0} +\beta\ket{1})$.</span></span> <span data-ttu-id="fdd97-173">Da es sich hierbei um die beabsichtigte __Nachricht__handelt, ist keine Änderung erforderlich.</span><span class="sxs-lookup"><span data-stu-id="fdd97-173">As this is the intended __message__, no alteration is required.</span></span>
* <span data-ttu-id="fdd97-174">Wenn wir gemessen und ein Ergebnis von 01 erhalten haben, befindet sich das dritte Qubit __dort__im Status $ (\alpha\ket{1} + \beta\ket{0}) $.</span><span class="sxs-lookup"><span data-stu-id="fdd97-174">If we measured and got a result of 01, then the third qubit, __there__, is in the state $(\alpha\ket{1} +\beta\ket{0})$.</span></span> <span data-ttu-id="fdd97-175">Dies unterscheidet sich von der vorgesehenen __Nachricht__, aber durch das Anwenden eines not-Gates erhält der gewünschte Zustand $ ({0} \alpha\ket +{1}\beta\ket) $.</span><span class="sxs-lookup"><span data-stu-id="fdd97-175">This differs from the intended __message__, however applying a NOT gate gives us the desired state $(\alpha\ket{0} +\beta\ket{1})$.</span></span>
* <span data-ttu-id="fdd97-176">Wenn wir gemessen und ein Ergebnis von 10 erhalten haben, befindet sich das dritte Qubit __dort__im Status $ (\alpha\ket{0} -\beta\ket{1}) $.</span><span class="sxs-lookup"><span data-stu-id="fdd97-176">If we measured and got a result of 10, then the third qubit, __there__, is in the state $(\alpha\ket{0} -\beta\ket{1})$.</span></span> <span data-ttu-id="fdd97-177">Dies unterscheidet sich von der vorgesehenen __Nachricht__, aber durch das Anwenden eines Z-Gates erhält der gewünschte Zustand $ ({0} \alpha\ket +{1}\beta\ket) $.</span><span class="sxs-lookup"><span data-stu-id="fdd97-177">This differs from the intended __message__, however applying a Z gate gives us the desired state $(\alpha\ket{0} +\beta\ket{1})$.</span></span>
* <span data-ttu-id="fdd97-178">Wenn wir gemessen haben und ein Ergebnis von 11 erhalten haben, __befindet sich das__dritte Qubit im Status $ (\alpha\ket{1} -\beta\ket{0}) $.</span><span class="sxs-lookup"><span data-stu-id="fdd97-178">If we measured and got a result of 11, then the third qubit, __there__, is in the state $(\alpha\ket{1} -\beta\ket{0})$.</span></span> <span data-ttu-id="fdd97-179">Dies unterscheidet sich von der vorgesehenen __Nachricht__, aber durch das Anwenden eines nicht-Gates gefolgt von einem Z-Gate erhält der gewünschte Zustand ${0} (\alpha\ket{1}+ \beta\ket) $.</span><span class="sxs-lookup"><span data-stu-id="fdd97-179">This differs from the intended __message__, however applying a NOT gate followed by a Z gate gives us the desired state $(\alpha\ket{0} +\beta\ket{1})$.</span></span>

<span data-ttu-id="fdd97-180">Zusammenfassend gilt: Wenn wir Messen und das erste Qubit den Wert 1 hat, wird ein Z-Gate angewendet.</span><span class="sxs-lookup"><span data-stu-id="fdd97-180">To summarize, if we measure and the first qubit is 1, a Z gate is applied.</span></span> <span data-ttu-id="fdd97-181">Wenn wir Messen und das zweite Qubit den Wert 1 hat, wird ein Not-Gate angewendet.</span><span class="sxs-lookup"><span data-stu-id="fdd97-181">If we measure and the second qubit is 1, a NOT gate is applied.</span></span>

### <a name="summary"></a><span data-ttu-id="fdd97-182">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="fdd97-182">Summary</span></span>
<span data-ttu-id="fdd97-183">Nachstehend sehen Sie eine Textbuch-Quantum-Verbindung, die die Teleportation implementiert.</span><span class="sxs-lookup"><span data-stu-id="fdd97-183">Shown below is a text-book quantum circuit that implements the teleportation.</span></span> <span data-ttu-id="fdd97-184">Wenn Sie von links nach rechts wechseln, sehen Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="fdd97-184">Moving from left to right you can see:</span></span>
- <span data-ttu-id="fdd97-185">Schritt 1: entwenden Sie __hier__ und __dort__ , indem Sie ein Hadamard-Gate und ein CNOT Gate anwenden.</span><span class="sxs-lookup"><span data-stu-id="fdd97-185">Step 1: Entangling __here__ and __there__ by applying a Hadamard gate and CNOT gate.</span></span>
- <span data-ttu-id="fdd97-186">Schritt 2: Senden der __Nachricht__ mit einem CNOT-Gate und einem Hadamard-Gate</span><span class="sxs-lookup"><span data-stu-id="fdd97-186">Step 2: Sending the __message__ using a CNOT gate and a Hadamard gate.</span></span>
- <span data-ttu-id="fdd97-187">Schritt 3: die Messung der ersten und zweiten Qubits, der __Nachricht__ und __hier__.</span><span class="sxs-lookup"><span data-stu-id="fdd97-187">Step 3: Taking a measurement of the first and second qubits, __message__ and __here__.</span></span>
- <span data-ttu-id="fdd97-188">Schritt 4: Anwenden eines nicht-Gates oder eines Z-Gates, abhängig vom Ergebnis der Messung in Schritt 3.</span><span class="sxs-lookup"><span data-stu-id="fdd97-188">Step 4: Applying a NOT gate or a Z gate, depending on the result of the measurement in step 3.</span></span>

![' Teleport (msg: Qubit, there: Qubit): Unit '](~/media/teleportation.svg)

## <a name="quantum-teleportation-code"></a><span data-ttu-id="fdd97-190">Quantum-Teleportation: Code</span><span class="sxs-lookup"><span data-stu-id="fdd97-190">Quantum Teleportation: Code</span></span>

<span data-ttu-id="fdd97-191">Wir haben unsere Verbindung für Quantum-Teleportation:</span><span class="sxs-lookup"><span data-stu-id="fdd97-191">We have our circuit for quantum teleportation:</span></span>

![' Teleport (msg: Qubit, there: Qubit): Unit '](~/media/teleportation.svg)

<span data-ttu-id="fdd97-193">Wir können nun jeden der Schritte in dieser Quantum-Leitung in Q # übersetzen.</span><span class="sxs-lookup"><span data-stu-id="fdd97-193">We can now translate each of the steps in this quantum circuit into Q#.</span></span>

### <a name="step-0-definition"></a><span data-ttu-id="fdd97-194">Schritt 0: Definition</span><span class="sxs-lookup"><span data-stu-id="fdd97-194">Step 0: Definition</span></span>
<span data-ttu-id="fdd97-195">Bei der Durchführung von Teleportationen müssen wir die __Nachricht__ kennen, die gesendet werden soll, und an welche Stelle wir Sie senden möchten (__dort__).</span><span class="sxs-lookup"><span data-stu-id="fdd97-195">When we perform teleportation, we must know the __message__ we wish to send, and where we wish to send it (__there__).</span></span> <span data-ttu-id="fdd97-196">Aus diesem Grund definieren wir zunächst einen neuen teleportvorgang, der zwei Qubits als Argumente `msg` erhält: `there`</span><span class="sxs-lookup"><span data-stu-id="fdd97-196">For this reason, we begin by defining a new Teleport operation that is given two qubits as arguments, `msg` and `there`:</span></span>

```qsharp
operation Teleport(msg : Qubit, there : Qubit) : Unit {
```

<span data-ttu-id="fdd97-197">Wir müssen auch ein Qubit `here` zuordnen, das wir mit einem `using` -Block erreichen:</span><span class="sxs-lookup"><span data-stu-id="fdd97-197">We also need to allocate a qubit `here` which we achieve with a `using` block:</span></span>

```qsharp
    using (here = Qubit()) {
```

### <a name="step-1-create-an-entangled-state"></a><span data-ttu-id="fdd97-198">Schritt 1: Erstellen eines entkoppelt-Zustands</span><span class="sxs-lookup"><span data-stu-id="fdd97-198">Step 1: Create an entangled state</span></span>
<span data-ttu-id="fdd97-199">Anschließend können wir das entkoppelte Paar zwischen `here` und `there` mit den @"microsoft.quantum.intrinsic.h" -und @"microsoft.quantum.intrinsic.cnot" -Vorgängen erstellen:</span><span class="sxs-lookup"><span data-stu-id="fdd97-199">We can then create the entangled pair between `here` and `there` by using the @"microsoft.quantum.intrinsic.h" and @"microsoft.quantum.intrinsic.cnot" operations:</span></span>

```qsharp
        H(here);
        CNOT(here, there);
```

### <a name="step-2-send-the-message"></a><span data-ttu-id="fdd97-200">Schritt 2: Senden der Nachricht</span><span class="sxs-lookup"><span data-stu-id="fdd97-200">Step 2: Send the message</span></span>
<span data-ttu-id="fdd97-201">Anschließend verwenden wir das nächste $ \operatschmue{CNOT} $ und $H $ Gates, um das Nachrichten-Qubit zu verschieben:</span><span class="sxs-lookup"><span data-stu-id="fdd97-201">We then use the next $\operatorname{CNOT}$ and $H$ gates to move our message qubit:</span></span>

```qsharp
        CNOT(msg, here);
        H(msg);
```

### <a name="step-3--4-measuring-and-interpreting-the-result"></a><span data-ttu-id="fdd97-202">Schritt 3 & 4: Messen und interpretieren des Ergebnisses</span><span class="sxs-lookup"><span data-stu-id="fdd97-202">Step 3 & 4: Measuring and interpreting the result</span></span>
<span data-ttu-id="fdd97-203">Schließlich verwenden @"microsoft.quantum.intrinsic.m" wir zum Durchführen der Messungen und zum Ausführen der erforderlichen Gate-Vorgänge, um den gewünschten Zustand zu erhalten, `if` wie durch-Anweisungen angegeben:</span><span class="sxs-lookup"><span data-stu-id="fdd97-203">Finally, we use @"microsoft.quantum.intrinsic.m" to perform the measurements and perform the necessary gate operations to get the desired state, as denoted by `if` statements:</span></span>

```qsharp
        // Measure out the entanglement
        if (M(msg) == One)  { Z(there); }
        if (M(here) == One) { X(there); }
```

### <a name="step-5-restarting-the-qubit-register"></a><span data-ttu-id="fdd97-204">Schritt 5: Neustarten des Qubit-Registers</span><span class="sxs-lookup"><span data-stu-id="fdd97-204">Step 5: Restarting the qubit register</span></span>

<span data-ttu-id="fdd97-205">Am Ende jedes Q #-Vorgangs müssen wir die Qubits im Status $ \ket{0}$ lassen.</span><span class="sxs-lookup"><span data-stu-id="fdd97-205">At the end of every Q# operation we need to let the qubits in the state $\ket{0}$.</span></span> <span data-ttu-id="fdd97-206">Wir können verwenden @"microsoft.quantum.intrinsic.reset" , um alle Qubits in den Zustand 0 (null) neu zu starten. Dadurch wird der Vorgang beendet.</span><span class="sxs-lookup"><span data-stu-id="fdd97-206">We can use @"microsoft.quantum.intrinsic.reset" to restart all the qubits to the zero state and this will finish our operation.</span></span>

```qsharp
        Reset(msg);
        Reset(here);
        Reset(there);
    }
}
```


