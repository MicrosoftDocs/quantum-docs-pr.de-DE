---
uid: Microsoft.Quantum.Synthesis.SizeAdjustedTruthTable
title: Sizeadjustedtruthtable-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: SizeAdjustedTruthTable
qsharp.summary: >-
  Adjusts truth table from array of Booleans according to number of variables

  A new array is returned of length `2^numVars`, possibly requiring to extend `table`'s size with `false` entries or truncating it to `2^numVars` elements.
ms.openlocfilehash: 8d69aa119c25a0f64743fec36c00ecdef2450c44
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855318"
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