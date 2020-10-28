---
title: Entwerfen Sie Ihren eigenen Klassifizierer mit dem QDK
description: Lernen Sie die grundlegenden Konzepte für das Entwerfen von Verbindungs Modellen für den Quantum Circuit zentrierten Klassifizierer kennen.
author: geduardo
ms.author: v-edsanc
ms.date: 02/17/2020
ms.topic: article
uid: microsoft.quantum.libraries.machine-learning.design
no-loc:
- ':::no-loc(Q#):::'
- ':::no-loc($$v):::'
ms.openlocfilehash: 221479e616ff7a03c4ac20e0062125660314e95b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92691149"
---
# <a name="design-your-own-classifier"></a><span data-ttu-id="c5286-103">Entwerfen Ihres eigenen Klassifizierers</span><span class="sxs-lookup"><span data-stu-id="c5286-103">Design your own classifier</span></span>

<span data-ttu-id="c5286-104">In diesem Handbuch lernen Sie die grundlegenden Konzepte kennen, die hinter dem Entwurf von Leitungs Modellen für den Quantum Circuit zentrischen Klassifizierer stehen.</span><span class="sxs-lookup"><span data-stu-id="c5286-104">In this guide you will learn the basic concepts behind the design of circuit models for the quantum circuit centric classifier.</span></span>

<span data-ttu-id="c5286-105">Wie bei klassischem Deep Learning gibt es keine allgemeine Regel für die Auswahl einer bestimmten Architektur.</span><span class="sxs-lookup"><span data-stu-id="c5286-105">As in classical deep learning, there is no general rule for choosing a specific architecture.</span></span> <span data-ttu-id="c5286-106">Abhängig vom Problem werden einige Architekturen besser als andere funktionieren.</span><span class="sxs-lookup"><span data-stu-id="c5286-106">Depending on the problem some architectures will perform better than others.</span></span> <span data-ttu-id="c5286-107">Es gibt jedoch einige Konzepte, die beim Entwerfen der Verbindung hilfreich sein könnten:</span><span class="sxs-lookup"><span data-stu-id="c5286-107">But, there are some concepts that might be useful when designing the circuit:</span></span>

- <span data-ttu-id="c5286-108">Eine große Anzahl von Parametern impliziert ein flexibleres Modell, das möglicherweise zum Zeichnen komplexer Klassifizierungs Grenzen geeignet ist, aber auch anfälliger für die über Anpassung ist.</span><span class="sxs-lookup"><span data-stu-id="c5286-108">A large number of parameters implies a more flexible model, which may be suitable to draw complicated classification boundaries but which may also be more susceptible to overfitting.</span></span>

- <span data-ttu-id="c5286-109">Das Entwirren von Gates zwischen Qubits ist für die Erfassung der Korrelationen zwischen den Quantum-Features von entscheidender Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="c5286-109">Entangling gates between qubits are essential to capture the correlations between the quantum features.</span></span>

## <a name="how-to-build-a-classifier-with-q"></a><span data-ttu-id="c5286-110">Erstellen eines Klassifizierers mit Q\#</span><span class="sxs-lookup"><span data-stu-id="c5286-110">How to build a classifier with Q\#</span></span>

<span data-ttu-id="c5286-111">Zum Erstellen einer Klassifizierer werden parametegesteuerte Rotationen in unserem Verbindungs Modell verkettet.</span><span class="sxs-lookup"><span data-stu-id="c5286-111">To build a classifier we are going to concatenate parametrized controlled rotations in our circuit model.</span></span> <span data-ttu-id="c5286-112">Hierfür können wir den [`ControlledRotation`](xref:Microsoft.Quantum.MachineLearning.ControlledRotation) in der Quantum-Machine Learning Bibliothek definierten Typ verwenden.</span><span class="sxs-lookup"><span data-stu-id="c5286-112">To do it we can use the type [`ControlledRotation`](xref:Microsoft.Quantum.MachineLearning.ControlledRotation) defined in the Quantum Machine Learning library.</span></span> <span data-ttu-id="c5286-113">Dieser Typ akzeptiert vier Argumente, die bestimmen: den Index des Ziel-Qubit, das Array von Indizes der Steuerelement-Qubits, die Achse der Drehung und den Index des zugeordneten Parameters im Array von Parametern, die das Modell definieren.</span><span class="sxs-lookup"><span data-stu-id="c5286-113">This type accepts four arguments that determine: the index of the target qubit, the array of indices of the control qubits, the axis of rotation, and index of the associated parameter in the array of parameters defining the model.</span></span>

<span data-ttu-id="c5286-114">Sehen wir uns ein Beispiel für einen Klassifizierer an.</span><span class="sxs-lookup"><span data-stu-id="c5286-114">Let's see an example of a classifier.</span></span> <span data-ttu-id="c5286-115">Im [Halbmond Beispiel](https://github.com/microsoft/Quantum/tree/main/samples/machine-learning/half-moons)finden Sie den folgenden Klassifizierer, der in der Datei definiert ist `Training.qs` .</span><span class="sxs-lookup"><span data-stu-id="c5286-115">In the [half-moons sample](https://github.com/microsoft/Quantum/tree/main/samples/machine-learning/half-moons), we can find the following classifier defined in the file `Training.qs`.</span></span>

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

<span data-ttu-id="c5286-116">Hier definieren wir eine Funktion, die ein Array von Elementen zurückgibt `ControlledRotation` , das mit einem Array von Parametern verknüpft ist, und ein Bias definiert das [`SequentialModel`](xref:Microsoft.Quantum.MachineLearning.SequentialModel) .</span><span class="sxs-lookup"><span data-stu-id="c5286-116">What we are defining here is a function that returns an array of `ControlledRotation` elements, that together with an array of parameters and a bias will define our [`SequentialModel`](xref:Microsoft.Quantum.MachineLearning.SequentialModel).</span></span> <span data-ttu-id="c5286-117">Dieser Typ ist in der Quantum-Machine Learning Bibliothek von grundlegender Bedeutung und definiert den Klassifizierer.</span><span class="sxs-lookup"><span data-stu-id="c5286-117">This type is fundamental in the Quantum Machine Learning library and defines the classifier.</span></span> <span data-ttu-id="c5286-118">Die in der obigen Funktion definierte Verbindung ist Teil eines Klassifizierers, in dem jede Stichprobe des Datasets zwei Funktionen enthält.</span><span class="sxs-lookup"><span data-stu-id="c5286-118">The circuit defined in the function above is part of a classifier in which each sample of the dataset contains two features.</span></span> <span data-ttu-id="c5286-119">Daher benötigen wir nur zwei Qubits.</span><span class="sxs-lookup"><span data-stu-id="c5286-119">Therefore we only need two qubits.</span></span> <span data-ttu-id="c5286-120">Die grafische Darstellung der Verbindung lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="c5286-120">The graphical representation of the circuit is:</span></span>

 ![Beispiel für Verbindungs Modell](~/media/circuit_model_1.PNG)

<span data-ttu-id="c5286-122">Beachten Sie, dass die Vorgänge der Quantum Machine Learning Library standardmäßig das letzte Qubit des Registers zum Schätzen der Klassifizierungs Wahrscheinlichkeiten messen.</span><span class="sxs-lookup"><span data-stu-id="c5286-122">Note that by default the operations of the Quantum Machine Learning library measure the last qubit of the register to estimate the classification probabilities.</span></span> <span data-ttu-id="c5286-123">Beachten Sie beim Entwerfen der Verbindung diese Tatsache.</span><span class="sxs-lookup"><span data-stu-id="c5286-123">You should keep in mind this fact when designing your circuit.</span></span>

## <a name="use-the-library-functions-to-write-layers-of-gates"></a><span data-ttu-id="c5286-124">Verwenden der Bibliotheksfunktionen zum Schreiben von Ebenen von Gates</span><span class="sxs-lookup"><span data-stu-id="c5286-124">Use the library functions to write layers of gates</span></span>

<span data-ttu-id="c5286-125">Angenommen, wir verfügen über ein DataSet mit 784-Features pro Instanz, z. b. Bilder mit 28 × 28 Pixeln wie dem mnist-DataSet.</span><span class="sxs-lookup"><span data-stu-id="c5286-125">Suppose we have a dataset with 784 features per instance, e.g. images of 28×28 pixels like the MNIST dataset.</span></span> <span data-ttu-id="c5286-126">In diesem Fall wird die Breite der Verbindung so groß, dass das manuelle Schreiben jedes einzelnen Gates zu einer möglichen, aber unpraktischen Aufgabe wird.</span><span class="sxs-lookup"><span data-stu-id="c5286-126">In this case, the width of the circuit becomes large enough so that writing by hand each individual gate becomes a possible but impractical task.</span></span> <span data-ttu-id="c5286-127">Aus diesem Grund stellt die Quantum-Machine Learning Bibliothek eine Reihe von Tools zum automatischen Generieren von Ebenen von parametersierten Rotationen bereit.</span><span class="sxs-lookup"><span data-stu-id="c5286-127">This is why the Quantum Machine Learning library provides a set of tools to automatically generate layers of parametrized rotations.</span></span> <span data-ttu-id="c5286-128">Die-Funktion gibt beispielsweise [`LocalRotationsLayer`](xref:Microsoft.Quantum.MachineLearning.LocalRotationsLayer) ein Array von unkontrollierten Single-Qubit-Drehungen an einer gegebenen Achse zurück, wobei für jedes Qubit im Register jeweils eine Drehung durch einen anderen Modellparameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="c5286-128">For instance, the function [`LocalRotationsLayer`](xref:Microsoft.Quantum.MachineLearning.LocalRotationsLayer) returns an array of uncontrolled single-qubit rotations along a given axis, with one rotation for each qubit in the register, each parametrized by a different model parameter.</span></span> <span data-ttu-id="c5286-129">Gibt beispielsweise `LocalRotationsLayer(4, X)` den folgenden Satz von Gates zurück:</span><span class="sxs-lookup"><span data-stu-id="c5286-129">For example, `LocalRotationsLayer(4, X)` returns the following set of gates:</span></span>

 ![Lokale rotationsebene](~/media/local_rotations_layer.PNG)

<span data-ttu-id="c5286-131">Wir empfehlen Ihnen, die [API-Referenz der Quantum Machine Learning Library](xref:Microsoft.Quantum.MachineLearning) zu erkunden, um alle verfügbaren Tools zum Optimieren des Leitungs Entwurfs zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="c5286-131">We recommend you explore the [API reference of the Quantum Machine Learning library](xref:Microsoft.Quantum.MachineLearning) to discover all the tools available to streamline the circuit design.</span></span>

## <a name="next-steps"></a><span data-ttu-id="c5286-132">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="c5286-132">Next steps</span></span>

 <span data-ttu-id="c5286-133">Testen Sie verschiedene Strukturen in den Beispielen, die von den Beispielen bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="c5286-133">Try different structures in the examples provided by the samples.</span></span> <span data-ttu-id="c5286-134">Werden Änderungen an der Leistung des Modells angezeigt?</span><span class="sxs-lookup"><span data-stu-id="c5286-134">Do you see any changes in the performance of the model?</span></span> <span data-ttu-id="c5286-135">Im nächsten Tutorial, [`Load your own datasets`](xref:microsoft.quantum.libraries.machine-learning.load) , erfahren Sie, wie Datasets geladen werden, um neue Architektur von Klassifizierern zu testen.</span><span class="sxs-lookup"><span data-stu-id="c5286-135">In the next tutorial, [`Load your own datasets`](xref:microsoft.quantum.libraries.machine-learning.load), you will learn how to load datasets to try and explore new architectures of classifiers.</span></span>
