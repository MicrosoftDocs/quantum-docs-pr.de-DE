---
uid: Microsoft.Quantum.MachineLearning.LabeledSample
title: Benutzerdefinierter Typ "labeledsample"
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: LabeledSample
qsharp.summary: A sample, labeled with a class to which that sample belongs.
ms.openlocfilehash: b357aae20b5bddb968ce1906fed3c1001efbfde7
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846981"
---
# <a name="labeledsample-user-defined-type"></a>Benutzerdefinierter Typ "labeledsample"

Namespace: [Microsoft. Quantum. machinelearning](xref:Microsoft.Quantum.MachineLearning)

Paket: [Microsoft. Quantum. machinelearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)


Ein Beispiel mit einer Klasse, zu der das Beispiel gehört.

```qsharp

newtype LabeledSample = (Features : Double[], Label : Int);
```



## <a name="named-items"></a>Benannte Elemente

### <a name="features--double"></a>Features: [Double](xref:microsoft.quantum.lang-ref.double)[]

Ein Vektor von Features für das angegebene Beispiel.
### <a name="label--int"></a>Bezeichnung: [int](xref:microsoft.quantum.lang-ref.int)

Eine ganzzahlige Bezeichnung für die Klasse, zu der dieses Beispiel gehört.