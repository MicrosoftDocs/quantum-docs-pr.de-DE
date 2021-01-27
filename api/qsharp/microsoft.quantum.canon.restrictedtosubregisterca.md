---
uid: Microsoft.Quantum.Canon.RestrictedToSubregisterCA
title: Restricteddesubregisterca-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: RestrictedToSubregisterCA
qsharp.summary: Restricts an operation to an array of indices of a register, i.e., a subregister. The modifier `CA` indicates that the operation is controllable and adjointable.
ms.openlocfilehash: 9b1c8a6d1c843fb0533af16aafc4b3ca2ba2f0e2
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98852173"
---
# <a name="restrictedtosubregisterca-function"></a>Restricteddesubregisterca-Funktion

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Schränkt einen Vorgang auf ein Array von Indizes eines Registers ein, d. h. ein unter Register.
Der-Modifizierer `CA` gibt an, dass der Vorgang steuerbar und adjointable ist.

```qsharp
function RestrictedToSubregisterCA (op : (Qubit[] => Unit is Adj + Ctl), idxs : Int[]) : (Qubit[] => Unit is Adj + Ctl)
```


## <a name="input"></a>Eingabe

### <a name="op--qubit--unit--is-adj--ctl"></a>OP: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL

Der Vorgang, der auf ein unter Register beschränkt werden soll.


### <a name="idxs--int"></a>idxs: [int](xref:microsoft.quantum.lang-ref.int)[]

Ein Array von Indizes, das angibt, auf welche Qubits der Vorgang beschränkt wird.



## <a name="output--qubit--unit--is-adj--ctl"></a>Ausgabe: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL



## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Canon. restricteddesubregister](xref:Microsoft.Quantum.Canon.RestrictedToSubregister)