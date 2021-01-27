---
uid: Microsoft.Quantum.Research.Chemistry._DeltaParityCNOTbitstring
title: _DeltaParityCNOTbitstring-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Research.Chemistry
qsharp.name: _DeltaParityCNOTbitstring
qsharp.summary: Classical processing step of `ApplyDeltaParity`. This computes a list of control qubits for evaluating parity difference between any two PQRS... terms of even length.
ms.openlocfilehash: 3dd2d299a094577d377780d731e76287815e8d03
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98847601"
---
# <a name="_deltaparitycnotbitstring-function"></a>_DeltaParityCNOTbitstring-Funktion

Namespace: [Microsoft. Quantum. Research. Chemistry](xref:Microsoft.Quantum.Research.Chemistry)

Paket: [Microsoft. Quantum. Research. Chemistry](https://nuget.org/packages/Microsoft.Quantum.Research.Chemistry)


Klassischer Verarbeitungsschritt von `ApplyDeltaParity` .
Dadurch wird eine Liste von Steuerungs-Qubits zum Auswerten der Paritäts Unterschiede zwischen zwei pqrs berechnet... Begriffe der geraden Länge.

```qsharp
function _DeltaParityCNOTbitstring (prevFermionicTerm : Int[], nextFermionicTerm : Int[]) : (Int, Bool[])
```


## <a name="input"></a>Eingabe

### <a name="prevfermionicterm--int"></a>prevfermionicterm: [int](xref:microsoft.quantum.lang-ref.int)[]




### <a name="nextfermionicterm--int"></a>nextfermionicterm: [int](xref:microsoft.quantum.lang-ref.int)[]





## <a name="output--intbool"></a>Ausgabe: ([int](xref:microsoft.quantum.lang-ref.int),[bool](xref:microsoft.quantum.lang-ref.bool)[])



## <a name="remarks"></a>Bemerkungen

Dabei wird davon ausgegangen, dass die Länge der Begriffe gleich ist.
Berechnet die Liste der Steuerelemente für den Paritäts Unterschied zwischen zwei Begriffen.
Dabei wird davon ausgegangen, dass die Eingabe Listen in aufsteigender Reihenfolge sortiert sind.