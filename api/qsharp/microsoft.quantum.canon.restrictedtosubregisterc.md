---
uid: Microsoft.Quantum.Canon.RestrictedToSubregisterC
title: Restrictedto subregisterc-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: RestrictedToSubregisterC
qsharp.summary: Restricts an operation to an array of indices of a register, i.e., a subregister. The modifier `C` indicates that the operation is controllable.
ms.openlocfilehash: 2ca32cf8c85f33f498a30f71833b3dd69db6da6e
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703842"
---
# <a name="restrictedtosubregisterc-function"></a>Restrictedto subregisterc-Funktion

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paketen [](https://nuget.org/packages/)


Schränkt einen Vorgang auf ein Array von Indizes eines Registers ein, d. h. ein unter Register.
Der-Modifizierer `C` gibt an, dass der Vorgang steuerbar ist.

```qsharp
function RestrictedToSubregisterC (op : (Qubit[] => Unit is Ctl), idxs : Int[]) : (Qubit[] => Unit is Ctl)
```


## <a name="input"></a>Eingabe

### <a name="op--qubit--unit-ctl"></a>OP: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) CTL

Der Vorgang, der auf ein unter Register beschränkt werden soll.


### <a name="idxs--int"></a>idxs: [int](xref:microsoft.quantum.lang-ref.int)[]

Ein Array von Indizes, das angibt, auf welche Qubits der Vorgang beschränkt wird.



## <a name="output--qubit--unit-ctl"></a>Ausgabe: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) CTL



## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Canon. restricteddesubregister](xref:Microsoft.Quantum.Canon.RestrictedToSubregister)