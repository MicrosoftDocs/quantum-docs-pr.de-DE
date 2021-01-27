---
uid: Microsoft.Quantum.MachineLearning.Misclassifications
title: Funktion "falsch Klassifizierungen"
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: Misclassifications
qsharp.summary: Given a set of inferred labels and a set of correct labels, returns indices for where each set of labels differs.
ms.openlocfilehash: 3913395fbd9f7cf96732c17ca0c726289e5087ed
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853929"
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

## <a name="example"></a>Beispiel

```qsharp
let misclassifications = Misclassifications([0, 1, 0, 0], [0, 1, 1, 0]);
Message($"{misclassifications}"); // Will print [2].
```