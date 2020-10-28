---
uid: Microsoft.Quantum.MachineLearning.LabeledSample
title: Benutzerdefinierter Typ "labeledsample"
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: LabeledSample
qsharp.summary: A sample, labeled with a class to which that sample belongs.
ms.openlocfilehash: 8b4afa1eaf7ca69938b2606163cd1ec17a1ad80f
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702053"
---
# <a name="labeledsample-user-defined-type"></a>Benutzerdefinierter Typ "labeledsample"

Namespace: [Microsoft. Quantum. machinelearning](xref:Microsoft.Quantum.MachineLearning)

Paketen [](https://nuget.org/packages/)


Ein Beispiel mit einer Klasse, zu der das Beispiel gehört.

```qsharp

newtype LabeledSample = (Features : Double[], Label : Int);
```



## <a name="named-items"></a>Benannte Elemente

### <a name="features--double"></a>Features: [Double](xref:microsoft.quantum.lang-ref.double)[]

Ein Vektor von Features für das angegebene Beispiel.
### <a name="label--int"></a>Bezeichnung: [int](xref:microsoft.quantum.lang-ref.int)

Eine ganzzahlige Bezeichnung für die Klasse, zu der dieses Beispiel gehört.