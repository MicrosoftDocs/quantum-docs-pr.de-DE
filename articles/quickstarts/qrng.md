---
title: Erstellen eines Quanten-Zufallszahlengenerators
description: Enthält eine Beschreibung der Erstellung eines Q#-Projekts, mit dem grundlegende Quantenkonzepte wie die Überlagerung veranschaulicht werden, indem ein Quanten-Zufallszahlengenerator erstellt wird.
author: bromeg
ms.author: megbrow@microsoft.com
ms.date: 10/25/2019
ms.topic: article
uid: microsoft.quantum.quickstarts.qrng
ms.openlocfilehash: c3039b92c4b3235a397d5cf31280ac2673706e9d
ms.sourcegitcommit: 2ca4755d1a63431e3cb2d2918a10ad477ec2e368
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2019
ms.locfileid: "73462838"
---
# <a name="quickstart-implement-a-quantum-random-number-generator-in-q"></a><span data-ttu-id="3e810-103">Schnellstart: Implementieren eines Quanten-Zufallszahlengenerators in Q#</span><span class="sxs-lookup"><span data-stu-id="3e810-103">Quickstart: Implement a Quantum Random Number Generator in Q#</span></span>
<span data-ttu-id="3e810-104">Ein einfaches Beispiel für einen Quantenalgorithmus, der in Q# geschrieben ist, ist ein Quanten-Zufallszahlengenerator.</span><span class="sxs-lookup"><span data-stu-id="3e810-104">A simple example of a quantum algorithm written in Q# is a quantum random number generator.</span></span> <span data-ttu-id="3e810-105">Für diesen Algorithmus wird das Prinzip der Quantenmechanik genutzt, um eine Zufallszahl zu generieren.</span><span class="sxs-lookup"><span data-stu-id="3e810-105">This algorithm leverages the nature of quantum mechanics to produce a random number.</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="3e810-106">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="3e810-106">Prerequisites</span></span>

- <span data-ttu-id="3e810-107">Das Microsoft [Quantum Development Kit](xref:microsoft.quantum.install).</span><span class="sxs-lookup"><span data-stu-id="3e810-107">The Microsoft [Quantum Development Kit](xref:microsoft.quantum.install).</span></span>
- [<span data-ttu-id="3e810-108">Erstellen eines Q#-Projekts</span><span class="sxs-lookup"><span data-stu-id="3e810-108">Create a Q# Project</span></span>](xref:microsoft.quantum.howto.createproject)


## <a name="write-a-q-operation"></a><span data-ttu-id="3e810-109">Schreiben einer Q#-Operation</span><span class="sxs-lookup"><span data-stu-id="3e810-109">Write a Q# operation</span></span>

### <a name="q-operation-code"></a><span data-ttu-id="3e810-110">Q#-Operationscode</span><span class="sxs-lookup"><span data-stu-id="3e810-110">Q# operation code</span></span>

1. <span data-ttu-id="3e810-111">Ersetzen Sie den Inhalt der Datei „Operation.qs“ durch den folgenden Code:</span><span class="sxs-lookup"><span data-stu-id="3e810-111">Replace the contents of the Operation.qs file with the following code:</span></span>

    ```qsharp
    namespace Quantum {
        open Microsoft.Quantum.Intrinsic;

        operation QuantumRandomNumberGenerator() : Result {
            using(q = Qubit())  { // Allocate a qubit.
                H(q);             // Put the qubit to superposition. It now has a 50% chance of being 0 or 1.
                let r = M(q);     // Measure the qubit value.
                Reset(q);
                return r;
            }
        }
    }
    ```

<span data-ttu-id="3e810-112">Wie im Artikel [Was ist Quantencomputing?](xref:microsoft.quantum.overview.what) erwähnt, stellt ein Qubit eine Einheit mit Quanteninformationen dar, für die eine Überlagerung vorliegen kann.</span><span class="sxs-lookup"><span data-stu-id="3e810-112">As mentioned in our [What is Quantum Computing?](xref:microsoft.quantum.overview.what) article, a qubit is a unit of quantum information that can be in superposition.</span></span> <span data-ttu-id="3e810-113">Für ein Qubit kann sich bei einer Messung nur 0 oder 1 ergeben.</span><span class="sxs-lookup"><span data-stu-id="3e810-113">When measured, a qubit can only be either 0 or 1.</span></span> <span data-ttu-id="3e810-114">Während der Ausführung steht der Zustand des Qubits aber für die Wahrscheinlichkeit, dass sich für eine Messung entweder 0 oder 1 ergibt.</span><span class="sxs-lookup"><span data-stu-id="3e810-114">However, during execution the state of the qubit represents the probability of reading either a 0 or a 1 with a measurement.</span></span> <span data-ttu-id="3e810-115">Dieser Wahrscheinlichkeitszustand wird als Überlagerung bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="3e810-115">This probabilistic state is known as superposition.</span></span> <span data-ttu-id="3e810-116">Wir können diese Wahrscheinlichkeit verwenden, um Zufallszahlen zu generieren.</span><span class="sxs-lookup"><span data-stu-id="3e810-116">We can use this probability to generate random numbers.</span></span>

<span data-ttu-id="3e810-117">In unserer Q#-Operation führen wir den nativen Q#-Datentyp `Qubit` ein.</span><span class="sxs-lookup"><span data-stu-id="3e810-117">In our Q# operation, we introduce the `Qubit` datatype, native to Q#.</span></span> <span data-ttu-id="3e810-118">Wir können `Qubit` nur mit einer `using`-Anweisung zuordnen.</span><span class="sxs-lookup"><span data-stu-id="3e810-118">We can only allocate a `Qubit` with a `using` statement.</span></span> <span data-ttu-id="3e810-119">Nach der Zuordnung befindet sich ein Qubit immer im Zustand `Zero`.</span><span class="sxs-lookup"><span data-stu-id="3e810-119">When it gets allocated a qubit is always in the `Zero`  state.</span></span> 

<span data-ttu-id="3e810-120">Mit der Operation `H` können wir das `Qubit` in den Zustand der Überlagerung versetzen.</span><span class="sxs-lookup"><span data-stu-id="3e810-120">Using the `H` operation, we are able to put our `Qubit` in superposition.</span></span> <span data-ttu-id="3e810-121">Zum Messen eines Qubits und Lesen seines Werts verwenden Sie die intrinsische Operation `M`.</span><span class="sxs-lookup"><span data-stu-id="3e810-121">To measure a qubit and read its value, you use the `M` intrinsic operation.</span></span>

<span data-ttu-id="3e810-122">Indem wir das `Qubit` in den Zustand der Überlagerung versetzen und die Messung durchführen, ergibt sich bei jedem Codeaufruf ein anderer Wert als Ergebnis.</span><span class="sxs-lookup"><span data-stu-id="3e810-122">By putting our `Qubit` in superposition and measuring it, our result will be a different value each time the code is invoked.</span></span> 

<span data-ttu-id="3e810-123">Wenn die Zuordnung für ein `Qubit` aufgehoben wird, muss es explizit zurück in den Zustand `Zero` versetzt werden. Andernfalls wird vom Simulator ein Laufzeitfehler gemeldet.</span><span class="sxs-lookup"><span data-stu-id="3e810-123">When a `Qubit` is de-allocated it must be explicitly set back to the `Zero` state, otherwise the simulator will report a runtime error.</span></span> <span data-ttu-id="3e810-124">Eine einfache Möglichkeit, dies zu erreichen, ist das Aufrufen von `Reset`.</span><span class="sxs-lookup"><span data-stu-id="3e810-124">An easy way to achieve this is invoking `Reset`.</span></span>

### <a name="visualizing-the-code-with-the-bloch-sphere"></a><span data-ttu-id="3e810-125">Visualisieren des Codes mit der Bloch-Kugel</span><span class="sxs-lookup"><span data-stu-id="3e810-125">Visualizing the code with the Bloch sphere</span></span>

<span data-ttu-id="3e810-126">Bei der Bloch-Kugel steht der Nordpol für den klassischen Wert **0** und der Südpol für den klassischen Wert **1**.</span><span class="sxs-lookup"><span data-stu-id="3e810-126">In the Bloch sphere the north pole represents the classical value **0** and the south pole represents the classical value **1**.</span></span> <span data-ttu-id="3e810-127">Jede Überlagerung kann durch einen Punkt auf der Kugel dargestellt werden (per Pfeil).</span><span class="sxs-lookup"><span data-stu-id="3e810-127">Any superposition can be represented by a point on the sphere (represented by an arrow).</span></span> <span data-ttu-id="3e810-128">Je näher sich das Ende des Pfeils an einem der Pole befindet, desto höher ist die Wahrscheinlichkeit, dass das Qubit bei einer Messung auf den klassischen Wert zurückfällt, der dem Pol zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="3e810-128">When the closer the end of the arrow to a pole, the higher the probability the qubit collapses into the classical value assigned to that pole when measured.</span></span> <span data-ttu-id="3e810-129">Der unten durch den roten Pfeil dargestellte Qubit-Zustand verfügt beispielsweise über eine höhere Wahrscheinlichkeit, dass sich bei einer Messung der Wert **0** ergibt.</span><span class="sxs-lookup"><span data-stu-id="3e810-129">For example, the qubit state represented by the red arrow below has a higher probability of giving the value **0** if we measure it.</span></span>

<img src="./Bloch.svg" width="175">

<span data-ttu-id="3e810-130">Wir können diese Darstellung verwenden, um die Aktivitäten des Codes zu visualisieren:</span><span class="sxs-lookup"><span data-stu-id="3e810-130">We can use this representation to visualize what the code is doing:</span></span>

* <span data-ttu-id="3e810-131">Wir beginnen mit einem im Zustand **0** initialisierten Qubit und wenden `H` an, um eine Überlagerung zu erstellen, bei der die Wahrscheinlichkeiten für **0** und **1** gleich hoch sind.</span><span class="sxs-lookup"><span data-stu-id="3e810-131">First we start with a qubit initalizated in the state **0** and apply `H` to create a superposition in which the probabilities for **0** and **1** are the same.</span></span>

<img src="./H.svg" width="450">

* <span data-ttu-id="3e810-132">Anschließend messen wir das Qubit und speichern die Ausgabe:</span><span class="sxs-lookup"><span data-stu-id="3e810-132">Then we measure the qubit and save the output:</span></span>

<img src="./Measurement2.svg" width="450">

<span data-ttu-id="3e810-133">Da das Ergebnis der Messung völlig zufällig ist, erhalten wir ein zufälliges Bit.</span><span class="sxs-lookup"><span data-stu-id="3e810-133">Since the outcome of the measurement is completely random, we have obtained a random bit.</span></span> <span data-ttu-id="3e810-134">Wir können diesen Vorgang mehrmals aufrufen, um ganze Zahlen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="3e810-134">We can call this operation several times to create integers.</span></span> <span data-ttu-id="3e810-135">Wenn wir den Vorgang beispielsweise dreimal aufrufen, um drei zufällige Bits zu erhalten, können wir zufällige 3-Bit-Zahlen erstellen (also eine Zufallszahl zwischen 0 und 7).</span><span class="sxs-lookup"><span data-stu-id="3e810-135">For example, if we call the operation three times to obtain three random bits, we can build random 3-bit numbers (that is, a random number between 0 and 7).</span></span>
