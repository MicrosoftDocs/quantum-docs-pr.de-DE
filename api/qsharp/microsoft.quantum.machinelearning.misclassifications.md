---
uid: Microsoft.Quantum.MachineLearning.Misclassifications
title: Funktion "falsch Klassifizierungen"
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: Misclassifications
qsharp.summary: Given a set of inferred labels and a set of correct labels, returns indices for where each set of labels differs.
ms.openlocfilehash: e13a9b9b65931678d5d87878e81fa172329a28ea
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96211677"
---
# <a name="misclassifications-function"></a>Funktion "falsch Klassifizierungen"

Namespace: [Microsoft. Quantum. machinelearning](xref:Microsoft.Quantum.MachineLearning)

Paket: [Microsoft. Quantum. machinelearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)


Gibt einen Satz von abhergenten Bezeichnungen und einen Satz korrekter Bezeichnungen zurück, wenn jeder Satz von Bezeichnungen abweicht.

```qsharp
function Misclassifications (inferredLabels : Int[], actualLabels : Int[]) : Int[]
```


## <a name="input"></a>Eingabe

### <a name="inferredlabels--int"></a>inferredlabels: [int](xref:microsoft.quantum.lang-ref.int)[]

Die Bezeichnungen, die für eine bestimmte Schulung oder einen bestimmten Validierungs Satz abgeleitet werden.


### <a name="actuallabels--int"></a>actuallabels: [int](xref:microsoft.quantum.lang-ref.int)[]

Die echten Bezeichnungen für eine bestimmte Schulung oder einen bestimmten Validierungs Satz.



## <a name="output--int"></a>Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)[]

Ein Array von Indizes `idx` , die den Wert haben `inferredLabels[idx] != actualLabels[idx]` .