---
uid: Microsoft.Quantum.Chemistry.JordanWigner._ComputeJordanWignerBitString
title: _ComputeJordanWignerBitString-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: _ComputeJordanWignerBitString
qsharp.summary: Computes Z component of Jordan–Wigner string between fermion indices in a fermionic operator with an even number of creation / annihilation operators.
ms.openlocfilehash: 82b5e433f79c93c640b89e6365e5f468bacd892e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98839524"
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

## <a name="example"></a>Beispiel

Let bitstring = _ComputeJordanWignerBitString (6, [0, 1, 2, 6]); bitstring ist [false, false, false, true, true, true, false].