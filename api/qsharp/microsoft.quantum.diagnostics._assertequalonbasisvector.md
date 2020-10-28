---
uid: Microsoft.Quantum.Diagnostics._assertEqualOnBasisVector
title: _assertEqualOnBasisVector Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: _assertEqualOnBasisVector
qsharp.summary: Checks if the result of applying two operations `givenU` and `expectedU` to a basis state is the same. The basis state is described by `basis` parameter. See <xref:microsoft.quantum.extensions.fliptobasis> function for more details on this description.
ms.openlocfilehash: 01b6d5aede102e47df86ea70d071d81eba1ade6f
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702833"
---
# <a name="_assertequalonbasisvector-operation"></a>_assertEqualOnBasisVector Vorgang

Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Paketen [](https://nuget.org/packages/)


Überprüft, ob das Ergebnis der Anwendung von zwei Vorgängen `givenU` und `expectedU` des Basis Zustands gleich ist. Der Basisstatus wird durch den- `basis` Parameter beschrieben.
<xref:microsoft.quantum.extensions.fliptobasis>Weitere Informationen zu dieser Beschreibung finden Sie unter function.

```qsharp
operation _assertEqualOnBasisVector (basis : Int[], givenU : (Qubit[] => Unit), expectedU : (Qubit[] => Unit is Adj)) : Unit
```


## <a name="input"></a>Eingabe

### <a name="basis--int"></a>Basis: [int](xref:microsoft.quantum.lang-ref.int)[]

Der durch eine Single-Qubit-Basis-ID angegebene Status-ID (0 <= ID <= 3) für jeden $n $ Qubits.


### <a name="givenu--qubit--unit"></a>givenu: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Einheit](xref:microsoft.quantum.lang-ref.unit) 

Der Vorgang auf $n $ Qubits, der geprüft werden soll.


### <a name="expectedu--qubit--unit-adj"></a>expectedu: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ

Verweis Vorgang auf $n $ Qubits, mit dem givenu verglichen werden soll.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)

