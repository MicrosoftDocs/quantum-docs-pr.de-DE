---
uid: Microsoft.Quantum.MachineLearning.DefaultTrainingOptions
title: Defaulttrainingoptions-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: DefaultTrainingOptions
qsharp.summary: Returns a default set of options for training classifiers.
ms.openlocfilehash: 474683ce5b9ec22bec686fb29d87728afe24d23a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98856008"
---
# <a name="defaulttrainingoptions-function"></a><span data-ttu-id="d08d9-102">Defaulttrainingoptions-Funktion</span><span class="sxs-lookup"><span data-stu-id="d08d9-102">DefaultTrainingOptions function</span></span>

<span data-ttu-id="d08d9-103">Namespace: [Microsoft. Quantum. machinelearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="d08d9-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="d08d9-104">Paket: [Microsoft. Quantum. machinelearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="d08d9-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="d08d9-105">Gibt einen Standardsatz von Optionen für Trainings Klassifizierer zurück.</span><span class="sxs-lookup"><span data-stu-id="d08d9-105">Returns a default set of options for training classifiers.</span></span>

```qsharp
function DefaultTrainingOptions () : Microsoft.Quantum.MachineLearning.TrainingOptions
```


## <a name="output--trainingoptions"></a><span data-ttu-id="d08d9-106">Ausgabe: [trainingoptions](xref:Microsoft.Quantum.MachineLearning.TrainingOptions)</span><span class="sxs-lookup"><span data-stu-id="d08d9-106">Output : [TrainingOptions](xref:Microsoft.Quantum.MachineLearning.TrainingOptions)</span></span>

<span data-ttu-id="d08d9-107">Ein angemessener Satz von Standard Schulungs Optionen, die beim Trainieren von Klassifizierungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d08d9-107">A reasonable set of default training options for use when training classifiers.</span></span>

## <a name="example"></a><span data-ttu-id="d08d9-108">Beispiel</span><span class="sxs-lookup"><span data-stu-id="d08d9-108">Example</span></span>

<span data-ttu-id="d08d9-109">Verwenden Sie den-Operator, um die Standardoptionen, aber mit zusätzlichen Messungen, zu verwenden `w/` :</span><span class="sxs-lookup"><span data-stu-id="d08d9-109">To use the default options, but with additional measurements, use the `w/` operator:</span></span>

```qsharp
let options = DefaultTrainingOptions()
    w/ NMeasurements <- 1000000;
```