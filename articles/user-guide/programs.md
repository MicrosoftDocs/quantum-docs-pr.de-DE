---
title: 'F #-Einführung'
description: 'Schnelle Einführung in Quantum-Programme in f #'
author: beheim
ms.author: beheim
ms.date: 11/08/2020
ms.topic: article
uid: microsoft.quantum.guide.programs
ms.openlocfilehash: 975bcda5e0042406b465a83f17f1d2d3f5a1ec4f
ms.sourcegitcommit: b930bb59a1ba8f41d2edc9ed98197109aa8c7f1b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96233974"
---
# <a name="q-quantum-programming-language"></a><span data-ttu-id="f2fad-103">Q # Quantum-Programmiersprache</span><span class="sxs-lookup"><span data-stu-id="f2fad-103">Q# Quantum Programming Language</span></span>

<span data-ttu-id="f2fad-104">Alles, was Sie über die Programmiersprache q # wissen müssen, ist im [f #](xref:microsoft.quantum.qsharp.index)-Programmiersprachen Handbuch ausführlich beschrieben.</span><span class="sxs-lookup"><span data-stu-id="f2fad-104">Everything you need to know about the Q# programming language is detailed in the [Q# language guide](xref:microsoft.quantum.qsharp.index).</span></span> <span data-ttu-id="f2fad-105">Wie bei allen anderen ist unser [sprach Entwurfsprozess](https://github.com/microsoft/qsharp-language#q-language-and-core-libraries-design) Open Source, und wir freuen uns auf Beiträge.</span><span class="sxs-lookup"><span data-stu-id="f2fad-105">Like anything else, our [language design process](https://github.com/microsoft/qsharp-language#q-language-and-core-libraries-design) is open source and we welcome contributions.</span></span>
<span data-ttu-id="f2fad-106">Weitere Hintergrundinformationen zu den Grundlagen und der Motivation hinter q # finden [Sie unter Warum benötigen wir q #?](https://devblogs.microsoft.com/qsharp/why-do-we-need-q/).</span><span class="sxs-lookup"><span data-stu-id="f2fad-106">For more background about the foundations and motivation behind Q#, see [Why do we need Q#?](https://devblogs.microsoft.com/qsharp/why-do-we-need-q/).</span></span>  
<span data-ttu-id="f2fad-107">Q # wird als Teil des Quantum Development Kit (QDK) bereitgestellt, um eine kurze Übersicht zu erhalten. Weitere Informationen finden Sie unter [Was ist das QDK?](xref:microsoft.quantum.overview.q-sharp).</span><span class="sxs-lookup"><span data-stu-id="f2fad-107">Q# is shipped as part of the Quantum Development Kit (QDK) For a quick overview, check out [What is the QDK?](xref:microsoft.quantum.overview.q-sharp).</span></span> 

## <a name="what-is-a-quantum-program"></a><span data-ttu-id="f2fad-108">Was ist ein Quantum-Programm?</span><span class="sxs-lookup"><span data-stu-id="f2fad-108">What is a quantum program?</span></span>

<span data-ttu-id="f2fad-109">Ein Quantum-Programm kann als ein bestimmter Satz klassischer Unterroutinen angesehen werden, die, wenn Sie aufgerufen werden, eine Berechnung durchführen, indem Sie mit einem Quantum-System interagieren. ein in Q # geschriebenes Programm modelliert den Quantenzustand nicht direkt, sondern beschreibt, wie ein klassischer Steuerungscomputer mit Qubits interagiert.</span><span class="sxs-lookup"><span data-stu-id="f2fad-109">A quantum program can be seen as a particular set of classical subroutines which, when called, perform a computation by interacting with a quantum system; a program written in Q# does not directly model the quantum state, but rather describes how a classical control computer interacts with qubits.</span></span>
<span data-ttu-id="f2fad-110">Dies ermöglicht es uns, unabhängig davon, was ein Quantum-Status *ist* , auch auf jedem Zielcomputer zu sein, der je nach Computer unterschiedliche Interpretationen aufweisen kann.</span><span class="sxs-lookup"><span data-stu-id="f2fad-110">This allows us to be entirely agnostic about what a quantum state even *is* on each target machine, which might have different interpretations depending on the machine.</span></span> 

<span data-ttu-id="f2fad-111">Eine wichtige Folge davon besteht darin, dass q # nicht in der Lage ist, den Zustand eines Qubit oder anderer Eigenschaften von Quantum-Mechanismen direkt zu überprüfen, was sicherstellt, dass ein q #-Programm physisch auf einem Quantum-Computer ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="f2fad-111">An important consequence of that is that Q# has no ability to introspect into the state of a qubit or other properties of quantum mechanics directly, which guarantees that a Q# program can be physically executed on a quantum computer.</span></span>
<span data-ttu-id="f2fad-112">Stattdessen kann ein Programm Vorgänge wie z. b [`Measure`](xref:Microsoft.Quantum.Intrinsic.Measure) . verwenden, um klassische Informationen aus einem Qubit zu extrahieren.</span><span class="sxs-lookup"><span data-stu-id="f2fad-112">Instead, a program can call operations such as [`Measure`](xref:Microsoft.Quantum.Intrinsic.Measure) to extract classical information from a qubit.</span></span>

<span data-ttu-id="f2fad-113">Nach dem zuordnen kann ein Qubit an Vorgänge und Funktionen weitergegeben werden, die auch als *callables* bezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="f2fad-113">Once allocated, a qubit can be passed to operations and functions, also referred to as *callables*.</span></span> <span data-ttu-id="f2fad-114">In gewisser Hinsicht ist dies alles, was ein Q #-Programm mit einem Qubit tun kann. Alle direkten Aktionen für den Zustand eines Qubit werden alle durch *intrinsische* callables definiert, [`X`](xref:Microsoft.Quantum.Intrinsic.X) wie [`H`](xref:Microsoft.Quantum.Intrinsic.H) z. b. und, d. h. Aufrufe, deren Implementierungen nicht in Q # definiert sind, sondern stattdessen vom Zielcomputer definiert werden.</span><span class="sxs-lookup"><span data-stu-id="f2fad-114">In some sense, this is all that a Q# program can do with a qubit; Any direct actions on state of a qubit are all defined by *intrinsic* callables such as [`X`](xref:Microsoft.Quantum.Intrinsic.X) and [`H`](xref:Microsoft.Quantum.Intrinsic.H) - i.e. callables whose implementations are not defined within Q# but are instead defined by the target machine.</span></span> <span data-ttu-id="f2fad-115">Diese Vorgänge *werden tatsächlich nur* vom Zielcomputer durchgeführt, mit dem das jeweilige Q #-Programm ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f2fad-115">What these operations actually *do* is only made concrete by the target machine we use to run the particular Q# program.</span></span>

<span data-ttu-id="f2fad-116">Wenn Sie das Programm z. b. in unserem [vollständigen Simulator](xref:microsoft.quantum.machines.full-state-simulator)ausführen, führt der Simulator die entsprechenden mathematischen Operationen für das simulierte Quantum-System aus.</span><span class="sxs-lookup"><span data-stu-id="f2fad-116">For example, if running the program on our [full-state simulator](xref:microsoft.quantum.machines.full-state-simulator), the simulator performs the corresponding mathematical operations to the simulated quantum system.</span></span>
<span data-ttu-id="f2fad-117">Wenn der Zielcomputer jedoch ein echter Quantum-Computer ist, wird der Quantum-Computer durch das aufrufen solcher Vorgänge in Q # an die Zukunft weitergeleitet, um die entsprechenden *echten* Vorgänge auf dem *realen* Quantum-System auszuführen (z. b. genau zeitgesteuerte Laserpulse).</span><span class="sxs-lookup"><span data-stu-id="f2fad-117">But looking toward the future, when the target machine is a real quantum computer, calling such operations in Q# will direct the quantum computer to perform the corresponding *real* operations on the *real* quantum system (e.g. precisely timed laser pulses).</span></span>

<span data-ttu-id="f2fad-118">Ein Q #-Programm kombiniert diese Vorgänge neu, wie von einem Zielcomputer definiert, um neue Vorgänge auf höherer Ebene zu erstellen, um die Quantum-Berechnung auszudrücken.</span><span class="sxs-lookup"><span data-stu-id="f2fad-118">A Q# program recombines these operations as defined by a target machine to create new, higher-level operations to express quantum computation.</span></span>
<span data-ttu-id="f2fad-119">Auf diese Weise vereinfacht f # das Ausdrücken der Logik zugrunde liegenden Quantum-und Hybrid-Quantum – klassische Algorithmen und ist gleichzeitig in Bezug auf die Struktur eines Ziel Computers oder Simulators allgemein.</span><span class="sxs-lookup"><span data-stu-id="f2fad-119">In this way, Q# makes it easy to express the logic underlying quantum and hybrid quantum–classical algorithms, while also being general with respect to the structure of a target machine or simulator.</span></span>

<span data-ttu-id="f2fad-120">Ein einfaches Beispiel ist das folgende Programm, das ein Qubit im $ \ket $-Zustand zuordnet {0} , dann einen Hadamard-Vorgang `H` darauf anwendet und das Ergebnis in der `PauliZ` Basis misst.</span><span class="sxs-lookup"><span data-stu-id="f2fad-120">A simple example is the following program, which allocates one qubit in the $\ket{0}$ state, then applies a Hadamard operation `H` to it and measures the result in the `PauliZ` basis.</span></span>

```qsharp
@EntryPoint()
operation MeasureOneQubit() : Result {
    // The following using block creates a fresh qubit and initializes it
    // in the |0〉 state.
    using (qubit = Qubit()) {
        // We apply a Hadamard operation H to the state, thereby preparing the
        // state 1 / sqrt(2) (|0〉 + |1〉).
        H(qubit);
        // Now we measure the qubit in Z-basis.
        let result = M(qubit);
        // As the qubit is now in an eigenstate of the measurement operator,
        // we reset the qubit before releasing it.
        if (result == One) { X(qubit); }
        // Finally, we return the result of the measurement.
        return result;
    }
}
```

<span data-ttu-id="f2fad-121">Unsere [Quantum-Katas](https://github.com/microsoft/QuantumKatas#introduction) sind eine gute Einführung in die [Quantum Computing-Konzepte](https://github.com/microsoft/QuantumKatas#quantum-computing-concepts-qubits-and-gates) , wie z. b. häufige Quantum-Vorgänge und das Bearbeiten von Qubits.</span><span class="sxs-lookup"><span data-stu-id="f2fad-121">Our [Quantum Katas](https://github.com/microsoft/QuantumKatas#introduction) give a good introduction on [Quantum Computing Concepts](https://github.com/microsoft/QuantumKatas#quantum-computing-concepts-qubits-and-gates) such as common quantum operations and how to manipulate qubits.</span></span> <span data-ttu-id="f2fad-122">Weitere Beispiele finden Sie auch in systeminternen [Vorgängen und Funktionen](xref:microsoft.quantum.libraries.standard.prelude).</span><span class="sxs-lookup"><span data-stu-id="f2fad-122">More examples can also be found in [Intrinsic Operations and Functions](xref:microsoft.quantum.libraries.standard.prelude).</span></span>



