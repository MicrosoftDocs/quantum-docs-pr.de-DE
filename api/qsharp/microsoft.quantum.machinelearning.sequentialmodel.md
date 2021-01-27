---
uid: Microsoft.Quantum.MachineLearning.SequentialModel
title: Sequentialmodel-benutzerdefinierter Typ
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: SequentialModel
qsharp.summary: Describes a quantum classifier model composed of a sequence of parameterized and controlled rotations, an assignment of rotation angles, and a bias between the two classes recognized by the model.
ms.openlocfilehash: ab9c121884e489b5d056285008c91c1ad70bb053
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854894"
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

## <a name="references"></a>References

- [arXiv: 1804.00633](https://arxiv.org/abs/1804.00633)