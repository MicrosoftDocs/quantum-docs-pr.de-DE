---
title: Entwerfen Sie Ihren eigenen Klassifizierer mit dem QDK
description: Lernen Sie die grundlegenden Konzepte für das Entwerfen von Verbindungs Modellen für den Quantum Circuit zentrierten Klassifizierer kennen.
author: geduardo
ms.author: v-edsanc@microsoft.com
ms.date: 02/17/2020
ms.topic: article
uid: microsoft.quantum.libraries.machine-learning.design
ms.openlocfilehash: 4899336f437c1b7712a7831b97fd6ec1431b59a2
ms.sourcegitcommit: 6ccea4a2006a47569c4e2c2cb37001e132f17476
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/28/2020
ms.locfileid: "77909720"
---
# <a name="design-your-own-classifier"></a><span data-ttu-id="616bc-103">Entwerfen Sie einen eigenen Klassifizierer</span><span class="sxs-lookup"><span data-stu-id="616bc-103">Design your own classifier</span></span>

<span data-ttu-id="616bc-104">In diesem Handbuch lernen Sie die grundlegenden Konzepte kennen, die hinter dem Entwurf von Leitungs Modellen für den Quantum Circuit zentrischen Klassifizierer stehen.</span><span class="sxs-lookup"><span data-stu-id="616bc-104">In this guide you will learn the basic concepts behind the design of circuit models for the quantum circuit centric classifier.</span></span>

<span data-ttu-id="616bc-105">Wie bei klassischem Deep Learning gibt es keine allgemeine Regel für die Auswahl einer bestimmten Architektur.</span><span class="sxs-lookup"><span data-stu-id="616bc-105">As in classical deep learning, there is no general rule for choosing a specific architecture.</span></span> <span data-ttu-id="616bc-106">Abhängig vom Problem werden einige Architekturen besser als andere funktionieren.</span><span class="sxs-lookup"><span data-stu-id="616bc-106">Depending on the problem some architectures will perform better than others.</span></span> <span data-ttu-id="616bc-107">Es gibt jedoch einige Konzepte, die beim Entwerfen der Verbindung hilfreich sein könnten:</span><span class="sxs-lookup"><span data-stu-id="616bc-107">But, there are some concepts that might be useful when designing the circuit:</span></span>

- <span data-ttu-id="616bc-108">Eine große Anzahl von Parametern impliziert ein flexibleres Modell, das möglicherweise zum Zeichnen komplexer Klassifizierungs Grenzen geeignet ist, aber auch anfälliger für die über Anpassung ist.</span><span class="sxs-lookup"><span data-stu-id="616bc-108">A large number of parameters implies a more flexible model, which may be suitable to draw complicated classification boundaries but which may also be more susceptible to overfitting.</span></span>

- <span data-ttu-id="616bc-109">Das Entwirren von Gates zwischen Qubits ist für die Erfassung der Korrelationen zwischen den Quantum-Features von entscheidender Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="616bc-109">Entangling gates between qubits are essential to capture the correlations between the quantum features.</span></span>

## <a name="how-to-build-a-classifier-with-q"></a><span data-ttu-id="616bc-110">Erstellen eines Klassifizierers mit Q-\#</span><span class="sxs-lookup"><span data-stu-id="616bc-110">How to build a classifier with Q\#</span></span>

<span data-ttu-id="616bc-111">Zum Erstellen einer Klassifizierer werden parametegesteuerte Rotationen in unserem Verbindungs Modell verkettet.</span><span class="sxs-lookup"><span data-stu-id="616bc-111">To build a classifier we are going to concatenate parametrized controlled rotations in our circuit model.</span></span> <span data-ttu-id="616bc-112">Hierfür können wir den Typ [`ControlledRotation`](xref:microsoft.quantum.machinelearning.controlledrotation) verwenden, der in der Quantum Machine Learning Library definiert ist.</span><span class="sxs-lookup"><span data-stu-id="616bc-112">To do it we can use the type [`ControlledRotation`](xref:microsoft.quantum.machinelearning.controlledrotation) defined in the Quantum Machine Learning library.</span></span> <span data-ttu-id="616bc-113">Dieser Typ akzeptiert vier Argumente, die bestimmen: den Index des Ziel-Qubit, das Array von Indizes der Steuerelement-Qubits, die Achse der Drehung und den Index des zugeordneten Parameters im Array von Parametern, die das Modell definieren.</span><span class="sxs-lookup"><span data-stu-id="616bc-113">This type accepts four arguments that determine: the index of the target qubit, the array of indices of the control qubits, the axis of rotation, and index of the associated parameter in the array of parameters defining the model.</span></span>

<span data-ttu-id="616bc-114">Sehen wir uns ein Beispiel für einen Klassifizierer an.</span><span class="sxs-lookup"><span data-stu-id="616bc-114">Let's see an example of a classifier.</span></span> <span data-ttu-id="616bc-115">Im [Halbmond Beispiel](https://github.com/microsoft/Quantum/tree/master/samples/machine-learning/half-moons)finden Sie den folgenden Klassifizierer, der in der Datei `Training.qs`definiert ist.</span><span class="sxs-lookup"><span data-stu-id="616bc-115">In the [half-moons sample](https://github.com/microsoft/Quantum/tree/master/samples/machine-learning/half-moons), we can find the following classifier defined in the file `Training.qs`.</span></span>

```qsharp
    function ClassifierStructure() : ControlledRotation[] {
        return [
            ControlledRotation((0, new Int[0]), PauliX, 4),
            ControlledRotation((0, new Int[0]), PauliZ, 5),
            ControlledRotation((1, new Int[0]), PauliX, 6),
            ControlledRotation((1, new Int[0]), PauliZ, 7),
            ControlledRotation((0, [1]), PauliX, 0),
            ControlledRotation((1, [0]), PauliX, 1),
            ControlledRotation((1, new Int[0]), PauliZ, 2),
            ControlledRotation((1, new Int[0]), PauliX, 3)
        ];
    }
 ```

<span data-ttu-id="616bc-116">Hier definieren wir eine Funktion, die ein Array von `ControlledRotation` Elementen zurückgibt, das mit einem Array von Parametern verknüpft ist, und ein Bias definiert unsere [`SequentialModel`](xref:microsoft.quantum.machinelearning.sequentialmodel).</span><span class="sxs-lookup"><span data-stu-id="616bc-116">What we are defining here is a function that returns an array of `ControlledRotation` elements, that together with an array of parameters and a bias will define our [`SequentialModel`](xref:microsoft.quantum.machinelearning.sequentialmodel).</span></span> <span data-ttu-id="616bc-117">Dieser Typ ist in der Quantum-Machine Learning Bibliothek von grundlegender Bedeutung und definiert den Klassifizierer.</span><span class="sxs-lookup"><span data-stu-id="616bc-117">This type is fundamental in the Quantum Machine Learning library and defines the classifier.</span></span> <span data-ttu-id="616bc-118">Die in der obigen Funktion definierte Verbindung ist Teil eines Klassifizierers, in dem jede Stichprobe des Datasets zwei Funktionen enthält.</span><span class="sxs-lookup"><span data-stu-id="616bc-118">The circuit defined in the function above is part of a classifier in which each sample of the dataset contains two features.</span></span> <span data-ttu-id="616bc-119">Daher benötigen wir nur zwei Qubits.</span><span class="sxs-lookup"><span data-stu-id="616bc-119">Therefore we only need two qubits.</span></span> <span data-ttu-id="616bc-120">Die grafische Darstellung der Verbindung lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="616bc-120">The graphical representation of the circuit is:</span></span>

 ![Beispiel für Verbindungs Modell](~/media/circuit_model_1.PNG)

## <a name="use-the-library-functions-to-write-layers-of-gates"></a><span data-ttu-id="616bc-122">Verwenden der Bibliotheksfunktionen zum Schreiben von Ebenen von Gates</span><span class="sxs-lookup"><span data-stu-id="616bc-122">Use the library functions to write layers of gates</span></span>

<span data-ttu-id="616bc-123">Angenommen, wir verfügen über ein DataSet mit 784-Features pro Instanz, z. b. Bilder mit 28 × 28 Pixeln wie dem mnist-DataSet.</span><span class="sxs-lookup"><span data-stu-id="616bc-123">Suppose we have a dataset with 784 features per instance, e.g. images of 28×28 pixels like the MNIST dataset.</span></span> <span data-ttu-id="616bc-124">In diesem Fall wird die Breite der Verbindung so groß, dass das manuelle Schreiben jedes einzelnen Gates zu einer möglichen, aber unpraktischen Aufgabe wird.</span><span class="sxs-lookup"><span data-stu-id="616bc-124">In this case, the width of the circuit becomes large enough so that writing by hand each individual gate becomes a possible but impractical task.</span></span> <span data-ttu-id="616bc-125">Aus diesem Grund stellt die Quantum-Machine Learning Bibliothek eine Reihe von Tools zum automatischen Generieren von Ebenen von parametersierten Rotationen bereit.</span><span class="sxs-lookup"><span data-stu-id="616bc-125">This is why the Quantum Machine Learning library provides a set of tools to automatically generate layers of parametrized rotations.</span></span> <span data-ttu-id="616bc-126">Beispielsweise gibt die-Funktion [`LocalRotationsLayer`](xref:microsoft.quantum.machinelearning.localrotationslayer) ein Array von unkontrollierten Single-Qubit-Drehungen an einer gegebenen Achse zurück, wobei für jedes Qubit im Register jeweils eine Drehung durch einen anderen Modellparameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="616bc-126">For instance, the function [`LocalRotationsLayer`](xref:microsoft.quantum.machinelearning.localrotationslayer) returns an array of uncontrolled single-qubit rotations along a given axis, with one rotation for each qubit in the register, each parametrized by a different model parameter.</span></span> <span data-ttu-id="616bc-127">`LocalRotationsLayer(4, X)` gibt beispielsweise den folgenden Satz von Gates zurück:</span><span class="sxs-lookup"><span data-stu-id="616bc-127">For example, `LocalRotationsLayer(4, X)` returns the following set of gates:</span></span>

 ![Lokale rotationsebene](~/media/local_rotations_layer.PNG)

<span data-ttu-id="616bc-129">Wir empfehlen Ihnen, die [API-Referenz der Quantum-Machine Learning Bibliothek](xref:microsoft.quantum.machinelearning) zu erkunden, um alle verfügbaren Tools zum Optimieren des Leitungs Entwurfs zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="616bc-129">We recommend you to explore the [API referenece of the Quantum Machine Learning library](xref:microsoft.quantum.machinelearning) to discover all the tools available to streamline the circuit design.</span></span>

## <a name="next-steps"></a><span data-ttu-id="616bc-130">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="616bc-130">Next steps</span></span>

 <span data-ttu-id="616bc-131">Testen Sie verschiedene Strukturen in den Beispielen, die von den Beispielen bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="616bc-131">Try different structures in the examples provided by the samples.</span></span> <span data-ttu-id="616bc-132">Werden Änderungen an der Leistung des Modells angezeigt?</span><span class="sxs-lookup"><span data-stu-id="616bc-132">Do you see any changes in the performance of the model?</span></span> <span data-ttu-id="616bc-133">Im nächsten Tutorial, [`Load your own datasets`](xref:microsoft.quantum.libraries.machine-learning.load), erfahren Sie, wie Datasets geladen werden, um neue Architektur von Klassifizierern zu testen.</span><span class="sxs-lookup"><span data-stu-id="616bc-133">In the next tutorial, [`Load your own datasets`](xref:microsoft.quantum.libraries.machine-learning.load), you will learn how to load datasets to try and explore new architectures of classifiers.</span></span>
