---
uid: Microsoft.Quantum.MachineLearning.LabeledSample
title: Benutzerdefinierter Typ "labeledsample"
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: LabeledSample
qsharp.summary: A sample, labeled with a class to which that sample belongs.
ms.openlocfilehash: a7c7dae5cd9e82d66bb98313f4200838006ca291
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96196326"
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