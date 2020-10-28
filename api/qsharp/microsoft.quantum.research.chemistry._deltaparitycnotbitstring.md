---
uid: Microsoft.Quantum.Research.Chemistry._DeltaParityCNOTbitstring
title: _DeltaParityCNOTbitstring-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Research.Chemistry
qsharp.name: _DeltaParityCNOTbitstring
qsharp.summary: Classical processing step of `ApplyDeltaParity`. This computes a list of control qubits for evaluating parity difference between any two PQRS... terms of even length.
ms.openlocfilehash: 95b4c2df05f32cb937ec2cf421f43f2fdbf319da
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92701844"
---
# <a name="_deltaparitycnotbitstring-function"></a>_DeltaParityCNOTbitstring-Funktion

Namespace: [Microsoft. Quantum. Research. Chemistry](xref:Microsoft.Quantum.Research.Chemistry)

Paketen [](https://nuget.org/packages/)


Klassischer Verarbeitungsschritt von `ApplyDeltaParity` .
Dadurch wird eine Liste von Steuerungs-Qubits zum Auswerten der Paritäts Unterschiede zwischen zwei pqrs berechnet... Begriffe der geraden Länge.

```qsharp
function _DeltaParityCNOTbitstring (prevFermionicTerm : Int[], nextFermionicTerm : Int[]) : (Int, Bool[])
```


## <a name="input"></a>Eingabe

### <a name="prevfermionicterm--int"></a>prevfermionicterm: [int](xref:microsoft.quantum.lang-ref.int)[]




### <a name="nextfermionicterm--int"></a>nextfermionicterm: [int](xref:microsoft.quantum.lang-ref.int)[]





## <a name="output--intbool"></a>Ausgabe: ([int](xref:microsoft.quantum.lang-ref.int),[bool](xref:microsoft.quantum.lang-ref.bool)[])



## <a name="remarks"></a>Hinweise

Dabei wird davon ausgegangen, dass die Länge der Begriffe gleich ist.
Berechnet die Liste der Steuerelemente für den Paritäts Unterschied zwischen zwei Begriffen.
Dabei wird davon ausgegangen, dass die Eingabe Listen in aufsteigender Reihenfolge sortiert sind.