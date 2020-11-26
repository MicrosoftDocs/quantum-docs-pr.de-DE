---
uid: Microsoft.Quantum.Chemistry.JordanWigner._ComputeJordanWignerBitString
title: _ComputeJordanWignerBitString-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: _ComputeJordanWignerBitString
qsharp.summary: Computes Z component of Jordan–Wigner string between fermion indices in a fermionic operator with an even number of creation / annihilation operators.
ms.openlocfilehash: 8121421a77174ef3e894381b281964b448e00a18
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96203942"
---
# <a name="_computejordanwignerbitstring-function"></a>_ComputeJordanWignerBitString-Funktion

Namespace: [Microsoft. Quantum. Chemistry. jordanwigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)

Paket: [Microsoft. Quantum. Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)


Berechnet die Z-Komponente von Jordanien – Wigner-Zeichenfolge zwischen Fermion-Indizes in einem fermionic-Operator mit einer geraden Anzahl von Erstellungs-/Vernichtungs Operatoren.

```qsharp
function _ComputeJordanWignerBitString (nFermions : Int, idxFermions : Int[]) : Bool[]
```


## <a name="input"></a>Eingabe

### <a name="nfermions--int"></a>nfermions: [int](xref:microsoft.quantum.lang-ref.int)

Die Anzahl der Fermionen im System.


### <a name="idxfermions--int"></a>idxfermions: [int](xref:microsoft.quantum.lang-ref.int)[]

fermionic-Operator Indizes.



## <a name="output--bool"></a>Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)[]

Bitzeichenfolge `Bool[]` , auf die `true` ein `PauliZ` angewendet werden soll.