---
uid: Microsoft.Quantum.Diagnostics.AssertOperationsEqualInPlaceCompBasis
title: Assertoperationsequalinplacecompbasis-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertOperationsEqualInPlaceCompBasis
qsharp.summary: Checks if the operation `givenU` is equal to the operation `expectedU` on the given input size  by checking the action of the operations only on the vectors from the computational basis. This is a necessary, but not sufficient, condition for the equality of two unitaries.
ms.openlocfilehash: f9d3aaf7e774cf2495ca69382db2470d1d0fa7b5
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98830481"
---
# <a name="assertoperationsequalinplacecompbasis-operation"></a>Assertoperationsequalinplacecompbasis-Vorgang

Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Überprüft, ob der Vorgang mit `givenU` dem Vorgang `expectedU` auf der angegebenen Eingabe Größe identisch ist, indem die Aktion der Vorgänge nur für die Vektoren von der Berechnungsbasis überprüft wird.
Dies ist eine erforderliche, aber nicht ausreichende Bedingung für die Gleichheit von zwei uniflüssen.

```qsharp
operation AssertOperationsEqualInPlaceCompBasis (nQubits : Int, givenU : (Qubit[] => Unit), expectedU : (Qubit[] => Unit is Adj)) : Unit
```


## <a name="input"></a>Eingabe

### <a name="nqubits--int"></a>nqubits: [int](xref:microsoft.quantum.lang-ref.int)

Die Anzahl der Qubits $n $, an denen die Vorgänge ausgeführt werden `givenU` `expectedU` .


### <a name="givenu--qubit--unit"></a>givenu: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Einheit](xref:microsoft.quantum.lang-ref.unit) 

Der Vorgang auf $n $ Qubits, der geprüft werden soll.


### <a name="expectedu--qubit--unit--is-adj"></a>expectedu: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ

Verweis Vorgang auf $n $ Qubits, der mit `givenU` verglichen werden soll.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)

