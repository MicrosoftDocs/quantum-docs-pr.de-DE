---
uid: Microsoft.Quantum.Canon.RestrictedToSubregisterA
title: Restricteddesubregistera-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: RestrictedToSubregisterA
qsharp.summary: Restricts an operation to an array of indices of a register, i.e., a subregister. The modifier `A` indicates that the operation is adjointable.
ms.openlocfilehash: c260a0e422d7ffb8137f6ac41e1cb398b2f4a2a7
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98852195"
---
# <a name="restrictedtosubregistera-function"></a>Restricteddesubregistera-Funktion

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Schränkt einen Vorgang auf ein Array von Indizes eines Registers ein, d. h. ein unter Register.
Der-Modifizierer `A` gibt an, dass der Vorgang adjointable ist.

```qsharp
function RestrictedToSubregisterA (op : (Qubit[] => Unit is Adj), idxs : Int[]) : (Qubit[] => Unit is Adj)
```


## <a name="input"></a>Eingabe

### <a name="op--qubit--unit--is-adj"></a>OP: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ

Der Vorgang, der auf ein unter Register beschränkt werden soll.


### <a name="idxs--int"></a>idxs: [int](xref:microsoft.quantum.lang-ref.int)[]

Ein Array von Indizes, das angibt, auf welche Qubits der Vorgang beschränkt wird.



## <a name="output--qubit--unit--is-adj"></a>Ausgabe: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ



## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Canon. restricteddesubregister](xref:Microsoft.Quantum.Canon.RestrictedToSubregister)