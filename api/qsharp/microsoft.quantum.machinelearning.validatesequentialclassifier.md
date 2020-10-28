---
uid: Microsoft.Quantum.MachineLearning.ValidateSequentialClassifier
title: Validatesequentialclassifier-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: ValidateSequentialClassifier
qsharp.summary: Validates a given sequential classifier against a given set of pre-labeled samples.
ms.openlocfilehash: 802f1045ea4086bd371d68018a481182cb75b209
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706826"
---
# <a name="validatesequentialclassifier-operation"></a><span data-ttu-id="1aa03-102">Validatesequentialclassifier-Vorgang</span><span class="sxs-lookup"><span data-stu-id="1aa03-102">ValidateSequentialClassifier operation</span></span>

<span data-ttu-id="1aa03-103">Namespace: [Microsoft. Quantum. machinelearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="1aa03-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="1aa03-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="1aa03-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="1aa03-105">Überprüft einen angegebenen sequenziellen Klassifizierer anhand eines angegebenen Satzes von vorbeschrifteten Beispielen.</span><span class="sxs-lookup"><span data-stu-id="1aa03-105">Validates a given sequential classifier against a given set of pre-labeled samples.</span></span>

```qsharp
operation ValidateSequentialClassifier (model : Microsoft.Quantum.MachineLearning.SequentialModel, samples : Microsoft.Quantum.MachineLearning.LabeledSample[], tolerance : Double, nMeasurements : Int, validationSchedule : Microsoft.Quantum.MachineLearning.SamplingSchedule) : Microsoft.Quantum.MachineLearning.ValidationResults
```


## <a name="input"></a><span data-ttu-id="1aa03-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="1aa03-106">Input</span></span>

### <a name="model--sequentialmodel"></a><span data-ttu-id="1aa03-107">Modell: [sequentialmodel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)</span><span class="sxs-lookup"><span data-stu-id="1aa03-107">model : [SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)</span></span>

<span data-ttu-id="1aa03-108">Das sequenzielle Modell, das überprüft werden soll.</span><span class="sxs-lookup"><span data-stu-id="1aa03-108">The sequential model to be validated.</span></span>


### <a name="samples--labeledsample"></a><span data-ttu-id="1aa03-109">Beispiele: [labeledsample](xref:Microsoft.Quantum.MachineLearning.LabeledSample)[]</span><span class="sxs-lookup"><span data-stu-id="1aa03-109">samples : [LabeledSample](xref:Microsoft.Quantum.MachineLearning.LabeledSample)[]</span></span>

<span data-ttu-id="1aa03-110">Die Beispiele, die zum Überprüfen des angegebenen Modells verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="1aa03-110">The samples to be used to validate the given model.</span></span>


### <a name="tolerance--double"></a><span data-ttu-id="1aa03-111">Toleranz: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="1aa03-111">tolerance : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="1aa03-112">Die Näherungs Toleranz, die beim Codieren der einzelnen Stichproben als Eingabe für den sequenziellen Klassifizierer verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1aa03-112">The approximation tolerance to use in encoding each sample as an input to the sequential classifier.</span></span>


### <a name="nmeasurements--int"></a><span data-ttu-id="1aa03-113">nmessungen: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="1aa03-113">nMeasurements : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="1aa03-114">Die Anzahl der für die Klassifizierung der einzelnen Stichproben zu verwendenden Messungen.</span><span class="sxs-lookup"><span data-stu-id="1aa03-114">The number of measurements to use in classifying each sample.</span></span>


### <a name="validationschedule--samplingschedule"></a><span data-ttu-id="1aa03-115">validationschedule: [samplingschedule](xref:Microsoft.Quantum.MachineLearning.SamplingSchedule)</span><span class="sxs-lookup"><span data-stu-id="1aa03-115">validationSchedule : [SamplingSchedule](xref:Microsoft.Quantum.MachineLearning.SamplingSchedule)</span></span>

<span data-ttu-id="1aa03-116">Der Zeitplan, nach dem Beispiele aus dem Validierungs Satz gezeichnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="1aa03-116">The schedule by which samples should be drawn from the validation set.</span></span>



## <a name="output--validationresults"></a><span data-ttu-id="1aa03-117">Ausgabe: [ValidationResults](xref:Microsoft.Quantum.MachineLearning.ValidationResults)</span><span class="sxs-lookup"><span data-stu-id="1aa03-117">Output : [ValidationResults](xref:Microsoft.Quantum.MachineLearning.ValidationResults)</span></span>

<span data-ttu-id="1aa03-118">Die Ergebnisse der angegebenen Validierung.</span><span class="sxs-lookup"><span data-stu-id="1aa03-118">The results of the given validation.</span></span>