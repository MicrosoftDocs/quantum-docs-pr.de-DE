---
uid: Microsoft.Quantum.MachineLearning.Misclassifications
title: Funktion "falsch Klassifizierungen"
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: Misclassifications
qsharp.summary: Given a set of inferred labels and a set of correct labels, returns indices for where each set of labels differs.
ms.openlocfilehash: 500c2910f7c5616c88ff6c70ab3cc16680e199fb
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92723578"
---
# <a name="misclassifications-function"></a>Funktion "falsch Klassifizierungen"

Namespace: [Microsoft. Quantum. machinelearning](xref:Microsoft.Quantum.MachineLearning)

Paketen [](https://nuget.org/packages/)


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