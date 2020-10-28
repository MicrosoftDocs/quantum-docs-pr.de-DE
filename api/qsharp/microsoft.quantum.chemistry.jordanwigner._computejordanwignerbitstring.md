---
uid: Microsoft.Quantum.Chemistry.JordanWigner._ComputeJordanWignerBitString
title: _ComputeJordanWignerBitString-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: _ComputeJordanWignerBitString
qsharp.summary: Computes Z component of Jordan–Wigner string between fermion indices in a fermionic operator with an even number of creation / annihilation operators.
ms.openlocfilehash: 31b957a435c3f578bc03d432609cde14c2ef5ced
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703494"
---
# <a name="_computejordanwignerbitstring-function"></a>_ComputeJordanWignerBitString-Funktion

Namespace: [Microsoft. Quantum. Chemistry. jordanwigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)

Paketen [](https://nuget.org/packages/)


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