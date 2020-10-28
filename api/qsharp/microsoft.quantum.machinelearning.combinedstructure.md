---
uid: Microsoft.Quantum.MachineLearning.CombinedStructure
title: Combinedstructure-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: CombinedStructure
qsharp.summary: Given one or more layers of controlled rotations, returns a single layer with model parameter index shifted such that distinct layers are parameterized by distinct model parameters.
ms.openlocfilehash: fbfd87761a40abe350e5f955fb53d8024eeb614e
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706874"
---
# <a name="combinedstructure-function"></a>Combinedstructure-Funktion

Namespace: [Microsoft. Quantum. machinelearning](xref:Microsoft.Quantum.MachineLearning)

Paketen [](https://nuget.org/packages/)


Bei einer oder mehreren Ebenen kontrollierter Drehungen gibt eine einzelne Ebene zurück, bei der der Modellparameter Index so verschoben wurde, dass unterschiedliche Ebenen von unterschiedlichen Modellparametern parametrisiert werden.

```qsharp
function CombinedStructure (layers : Microsoft.Quantum.MachineLearning.ControlledRotation[][]) : Microsoft.Quantum.MachineLearning.ControlledRotation[]
```


## <a name="input"></a>Eingabe

### <a name="layers--controlledrotation"></a>Ebenen: [controlledrotation](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[] []

Die zu kombinierenden Ebenen.



## <a name="output--controlledrotation"></a>Ausgabe: [controlledrotation](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[]

Eine einzelne Ebene von kontrollierten Rotationen, die die Verkettung aller anderen Ebenen darstellt.