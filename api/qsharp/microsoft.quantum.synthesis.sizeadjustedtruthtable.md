---
uid: Microsoft.Quantum.Synthesis.SizeAdjustedTruthTable
title: Sizeadjustedtruthtable-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: SizeAdjustedTruthTable
qsharp.summary: >-
  Adjusts truth table from array of Booleans according to number of variables

  A new array is returned of length `2^numVars`, possibly requiring to extend `table`'s size with `false` entries or truncating it to `2^numVars` elements.
ms.openlocfilehash: c53ac3f2c46bca955847fc7b380337e3910390ac
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96202922"
---
# <a name="sizeadjustedtruthtable-function"></a>Sizeadjustedtruthtable-Funktion

Namespace: [Microsoft. Quantum. Synthese](xref:Microsoft.Quantum.Synthesis)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Passt die Wahrheitstabelle anhand der Anzahl von Variablen aus einem Array von booleschen Werten an.

Ein neues Array wird von der Länge zurückgegeben. es ist `2^numVars` möglicherweise erforderlich, `table` die Größe durch Einträge zu erweitern `false` oder Sie auf Elemente zu kürzen `2^numVars` .

```qsharp
function SizeAdjustedTruthTable (table : Bool[], numVars : Int) : Bool[]
```


## <a name="input"></a>Eingabe

### <a name="table--bool"></a>Tabelle: [bool](xref:microsoft.quantum.lang-ref.bool)[]

Wahrheitstabelle als Array von Wahrheits Werten


### <a name="numvars--int"></a>numvars: [int](xref:microsoft.quantum.lang-ref.int)

Anzahl von Variablen



## <a name="output--bool"></a>Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)[]

Größe der angepassten Wahrheitstabelle