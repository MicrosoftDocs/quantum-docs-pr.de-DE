---
uid: Microsoft.Quantum.MachineLearning.SequentialModel
title: Sequentialmodel-benutzerdefinierter Typ
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: SequentialModel
qsharp.summary: Describes a quantum classifier model composed of a sequence of parameterized and controlled rotations, an assignment of rotation angles, and a bias between the two classes recognized by the model.
ms.openlocfilehash: 3afdb8dafe0179535fe5d8c3dff668f1f3de2f7d
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96196173"
---
# <a name="sequentialmodel-user-defined-type"></a>Sequentialmodel-benutzerdefinierter Typ

Namespace: [Microsoft. Quantum. machinelearning](xref:Microsoft.Quantum.MachineLearning)

Paket: [Microsoft. Quantum. machinelearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)


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