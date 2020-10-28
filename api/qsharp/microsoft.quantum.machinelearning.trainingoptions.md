---
uid: Microsoft.Quantum.MachineLearning.TrainingOptions
title: Trainingoptions-benutzerdefinierter Typ
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: TrainingOptions
qsharp.summary: A collection of options to be used in training quantum classifiers.
ms.openlocfilehash: 5ecc2b5175a4e8db78f72311ac1d5ff964bae811
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92722374"
---
# <a name="trainingoptions-user-defined-type"></a><span data-ttu-id="c88b9-102">Trainingoptions-benutzerdefinierter Typ</span><span class="sxs-lookup"><span data-stu-id="c88b9-102">TrainingOptions user defined type</span></span>

<span data-ttu-id="c88b9-103">Namespace: [Microsoft. Quantum. machinelearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="c88b9-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="c88b9-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="c88b9-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="c88b9-105">Eine Auflistung von Optionen, die beim Trainieren von Quantum Classifiers verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c88b9-105">A collection of options to be used in training quantum classifiers.</span></span>

```qsharp

newtype TrainingOptions = (LearningRate : Double, Tolerance : Double, MinibatchSize : Int, NMeasurements : Int, MaxEpochs : Int, MaxStalls : Int, StochasticRescaleFactor : Double, ScoringPeriod : Int, VerboseMessage : (String -> Unit));
```



## <a name="named-items"></a><span data-ttu-id="c88b9-106">Benannte Elemente</span><span class="sxs-lookup"><span data-stu-id="c88b9-106">Named Items</span></span>

### <a name="learningrate--double"></a><span data-ttu-id="c88b9-107">Learningrate: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="c88b9-107">LearningRate : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="c88b9-108">Die Lernrate, mit der Gradienten beim Aktualisieren von Modellparametern während der Trainingsschritte neu berechnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c88b9-108">The learning rate by which gradients should be rescaled when updating model parameters during training steps.</span></span>
### <a name="tolerance--double"></a><span data-ttu-id="c88b9-109">Toleranz: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="c88b9-109">Tolerance : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="c88b9-110">Die Näherungs Toleranz, die beim Vorbereiten von Beispielen als quantale Zustände verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c88b9-110">The approximation tolerance to use when preparing samples as quantum states.</span></span>
### <a name="minibatchsize--int"></a><span data-ttu-id="c88b9-111">Minibatchsize: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="c88b9-111">MinibatchSize : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="c88b9-112">Die Anzahl der Samplings, die in den einzelnen Trainings-minibatches verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c88b9-112">The number of samples to use in each training minibatch.</span></span>
### <a name="nmeasurements--int"></a><span data-ttu-id="c88b9-113">Nmessungen: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="c88b9-113">NMeasurements : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="c88b9-114">Gibt an, wie oft jedes Klassifizierungs Ergebnis gemessen werden soll, um die Klassifizierungs Wahrscheinlichkeit einzuschätzen.</span><span class="sxs-lookup"><span data-stu-id="c88b9-114">The number of times to measure each classification result in order to estimate the classification probability.</span></span>
### <a name="maxepochs--int"></a><span data-ttu-id="c88b9-115">Maxepochen: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="c88b9-115">MaxEpochs : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="c88b9-116">Die maximale Anzahl von Epochen, für die jedes Modell trainiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="c88b9-116">The maximum number of epochs to train each model for.</span></span>
### <a name="maxstalls--int"></a><span data-ttu-id="c88b9-117">Maxstems: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="c88b9-117">MaxStalls : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="c88b9-118">Die maximale Anzahl von Verläufen für eine Trainings Epoche (ungefähr 0 (null)), bevor ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="c88b9-118">The maximum number of times a training epoch is allowed to stall (approximately zero gradient) before failing.</span></span>
### <a name="stochasticrescalefactor--double"></a><span data-ttu-id="c88b9-119">Stochastikrescalefactor: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="c88b9-119">StochasticRescaleFactor : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="c88b9-120">Der Betrag für das erneute Skalieren von mit dem Gerät abgehaltenen Modellen durch vor dem erneuten Ausführen</span><span class="sxs-lookup"><span data-stu-id="c88b9-120">The amount to rescale stalled models by before retrying an update.</span></span>
### <a name="scoringperiod--int"></a><span data-ttu-id="c88b9-121">Scoringperiod: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="c88b9-121">ScoringPeriod : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="c88b9-122">Die Anzahl der Verlaufs Schritte, die zwischen Bewertungs Punkten durchgeführt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c88b9-122">The number of gradient steps to be taken between scoring points.</span></span>
<span data-ttu-id="c88b9-123">Legen Sie für optimale Genauigkeit den Wert 1 fest.</span><span class="sxs-lookup"><span data-stu-id="c88b9-123">For best accuracy, set to 1.</span></span>
### <a name="verbosemessage--string---unit"></a><span data-ttu-id="c88b9-124">Verbotmessage: [Zeichen](xref:microsoft.quantum.lang-ref.string) folgen -> [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="c88b9-124">VerboseMessage : [String](xref:microsoft.quantum.lang-ref.string) -> [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

<span data-ttu-id="c88b9-125">Eine Funktion, die verwendet werden kann, um ausführliche Rückmeldungen bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="c88b9-125">A function that can be used to provide verbose feedback.</span></span>

## <a name="remarks"></a><span data-ttu-id="c88b9-126">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c88b9-126">Remarks</span></span>

<span data-ttu-id="c88b9-127">Dieser UDT sollte nicht direkt erstellt werden, sondern sollte stattdessen durch Aufrufen von angegeben werden @"microsoft.quantum.machinelearning.defaulttrainingoptions" . Anschließend wird der- `w/` Operator verwendet, um andere Standardwerte zu überschreiben.</span><span class="sxs-lookup"><span data-stu-id="c88b9-127">This UDT should not be created directly, but rather should be specified by calling @"microsoft.quantum.machinelearning.defaulttrainingoptions" and then using the `w/` operator to override different defaults.</span></span>

<span data-ttu-id="c88b9-128">Beispielsweise, um 100.000 Messungen und höchstens 8 Schulungs Epochen zu verwenden:</span><span class="sxs-lookup"><span data-stu-id="c88b9-128">For example, to use 100,000 measurements and at most 8 training epochs:</span></span>

```Q#
let options = DefaultTrainingOptions()
              w/ NMeasurements <- 100000
              w/ MaxEpochs <- 8;
```

## <a name="references"></a><span data-ttu-id="c88b9-129">Referenzen</span><span class="sxs-lookup"><span data-stu-id="c88b9-129">References</span></span>

- [<span data-ttu-id="c88b9-130">arXiv: 1804.00633</span><span class="sxs-lookup"><span data-stu-id="c88b9-130">arXiv:1804.00633</span></span>](https://arxiv.org/abs/1804.00633)