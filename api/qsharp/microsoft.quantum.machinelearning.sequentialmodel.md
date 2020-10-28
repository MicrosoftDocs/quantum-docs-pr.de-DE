---
uid: Microsoft.Quantum.MachineLearning.SequentialModel
title: Sequentialmodel-benutzerdefinierter Typ
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: SequentialModel
qsharp.summary: Describes a quantum classifier model composed of a sequence of parameterized and controlled rotations, an assignment of rotation angles, and a bias between the two classes recognized by the model.
ms.openlocfilehash: a425d2155489384ca81ef1c00a5e842bcfb40ae7
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92722388"
---
# <a name="sequentialmodel-user-defined-type"></a>Sequentialmodel-benutzerdefinierter Typ

Namespace: [Microsoft. Quantum. machinelearning](xref:Microsoft.Quantum.MachineLearning)

Paketen [](https://nuget.org/packages/)


Beschreibt ein Quantum Klassifizierungs-Modell, das aus einer Sequenz von parametrisierten und kontrollierten Drehungen, einer Zuweisung von Drehwinkeln und einer Abweichung zwischen den beiden vom Modell erkannten Klassen besteht.

```qsharp

newtype SequentialModel = (Structure : Microsoft.Quantum.MachineLearning.ControlledRotation[], Parameters : Double[], Bias : Double);
```



## <a name="named-items"></a>Benannte Elemente

### <a name="structure--controlledrotation"></a>Struktur: [controlledrotation](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[]

Die Sequenz der kontrollierten Drehungen, die zum Klassifizieren von Eingaben verwendet werden.
### <a name="parameters--double"></a>Parameter: [Double](xref:microsoft.quantum.lang-ref.double)[]

Eine Zuweisung der Drehwinkel zur angegebenen Klassifizierungs Struktur.
### <a name="bias--double"></a>Bias: [Double](xref:microsoft.quantum.lang-ref.double)

Die Abweichung zwischen den beiden Klassen, die von diesem Klassifizierer erkannt werden.

## <a name="references"></a>Referenzen

- [arXiv: 1804.00633](https://arxiv.org/abs/1804.00633)