---
uid: Microsoft.Quantum.MachineLearning.NMisclassifications
title: Nfehllassikationen-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: NMisclassifications
qsharp.summary: Given a set of inferred labels and a set of correct labels, returns the number of indices at which each set of labels differ.
ms.openlocfilehash: 9e356d68233519978e007e5a2999ca1be8cb7f83
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92701369"
---
# <a name="nmisclassifications-function"></a>Nfehllassikationen-Funktion

Namespace: [Microsoft. Quantum. machinelearning](xref:Microsoft.Quantum.MachineLearning)

Paketen [](https://nuget.org/packages/)


Gibt die Anzahl der Indizes zurück, bei denen sich die einzelnen Bezeichnungen unterscheiden, wenn eine Reihe von abhergelegten Bezeichnungen und ein Satz korrekter Bezeichnungen angegeben sind.

```qsharp
function NMisclassifications (proposed : Int[], actual : Int[]) : Int
```


## <a name="input"></a>Eingabe

### <a name="proposed--int"></a>vorgeschlagen: [int](xref:microsoft.quantum.lang-ref.int)[]




### <a name="actual--int"></a>tatsächlicher Wert: [int](xref:microsoft.quantum.lang-ref.int)[]





## <a name="output--int"></a>Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)

Die Anzahl der Indizes `idx` `inferredLabels[idx] != actualLabels[idx]` .