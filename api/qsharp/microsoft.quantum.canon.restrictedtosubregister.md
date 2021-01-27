---
uid: Microsoft.Quantum.Canon.RestrictedToSubregister
title: Restricteddesubregister-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: RestrictedToSubregister
qsharp.summary: Restricts an operation to an array of indices of a register, i.e., a subregister.
ms.openlocfilehash: c5a6bbe16d2f6a317f6ed6f258077095465995f9
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840227"
---
# <a name="restrictedtosubregister-function"></a>Restricteddesubregister-Funktion

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Schränkt einen Vorgang auf ein Array von Indizes eines Registers ein, d. h. ein unter Register.

```qsharp
function RestrictedToSubregister (op : (Qubit[] => Unit), idxs : Int[]) : (Qubit[] => Unit)
```


## <a name="input"></a>Eingabe

### <a name="op--qubit--unit"></a>OP: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Einheit](xref:microsoft.quantum.lang-ref.unit) 

Der Vorgang, der auf ein unter Register beschränkt werden soll.


### <a name="idxs--int"></a>idxs: [int](xref:microsoft.quantum.lang-ref.int)[]

Ein Array von Indizes, das angibt, auf welche Qubits der Vorgang beschränkt wird.



## <a name="output--qubit--unit"></a>Ausgabe: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Einheit](xref:microsoft.quantum.lang-ref.unit) 



## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Canon. restricteddesubregistera](xref:Microsoft.Quantum.Canon.RestrictedToSubregisterA)
- [Microsoft. Quantum. Canon. restrictedto subregisterc](xref:Microsoft.Quantum.Canon.RestrictedToSubregisterC)
- [Microsoft. Quantum. Canon. restrictedto subregisterca](xref:Microsoft.Quantum.Canon.RestrictedToSubregisterCA)