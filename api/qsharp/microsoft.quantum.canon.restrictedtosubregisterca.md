---
uid: Microsoft.Quantum.Canon.RestrictedToSubregisterCA
title: Restricteddesubregisterca-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: RestrictedToSubregisterCA
qsharp.summary: Restricts an operation to an array of indices of a register, i.e., a subregister. The modifier `CA` indicates that the operation is controllable and adjointable.
ms.openlocfilehash: e81193a85451b72a69a595fa81a9fb07f3038c22
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703848"
---
# <a name="restrictedtosubregisterca-function"></a>Restricteddesubregisterca-Funktion

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paketen [](https://nuget.org/packages/)


Schränkt einen Vorgang auf ein Array von Indizes eines Registers ein, d. h. ein unter Register.
Der-Modifizierer `CA` gibt an, dass der Vorgang steuerbar und adjointable ist.

```qsharp
function RestrictedToSubregisterCA (op : (Qubit[] => Unit is Adj + Ctl), idxs : Int[]) : (Qubit[] => Unit is Adj + Ctl)
```


## <a name="input"></a>Eingabe

### <a name="op--qubit--unit-adj--ctl"></a>OP: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL

Der Vorgang, der auf ein unter Register beschränkt werden soll.


### <a name="idxs--int"></a>idxs: [int](xref:microsoft.quantum.lang-ref.int)[]

Ein Array von Indizes, das angibt, auf welche Qubits der Vorgang beschränkt wird.



## <a name="output--qubit--unit-adj--ctl"></a>Ausgabe: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL



## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Canon. restricteddesubregister](xref:Microsoft.Quantum.Canon.RestrictedToSubregister)