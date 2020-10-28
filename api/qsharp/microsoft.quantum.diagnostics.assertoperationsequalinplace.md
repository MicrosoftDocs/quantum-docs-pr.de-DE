---
uid: Microsoft.Quantum.Diagnostics.AssertOperationsEqualInPlace
title: Assertoperationsequalinplace-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertOperationsEqualInPlace
qsharp.summary: >-
  Given two operations, asserts that they act identically for all input states.

  This assertion is implemented by checking the action of the operations on all states of the form $V_0 \otimes ... \otimes V_{n-1}$, where $V_k$ is one of the states $\ket{0}$, $\ket{1}$, $\ket{+}$ and $\ket{i}$ (+1 eigenstate of Pauli Y operator).

  This assertion uses $n$ qubits and requires multiple calls of the operations being compared.
ms.openlocfilehash: 407a139da816281346eb06849f81e91b83202653
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702755"
---
# <a name="assertoperationsequalinplace-operation"></a>Assertoperationsequalinplace-Vorgang

Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Paketen [](https://nuget.org/packages/)


Bei zwei Vorgängen wird von bestätigt, dass Sie für alle Eingabe Zustände identisch agieren.

Diese Assertionen werden implementiert, indem die Aktion der Vorgänge für alle Zustände der Form $V _0 \otimes... \otimes v_ {n-1} $, wobei $V _K $ einem der Zustände $ \ket {0} $, $ \ket {1} $, $ \ket{+} $ und $ \ket{i} $ (+ 1 eigen Status des Pauli Y-Operators) entspricht.

Diese Assertion verwendet $n $ Qubits und erfordert mehrere Aufrufe der zu vergleichenden Vorgänge.

```qsharp
operation AssertOperationsEqualInPlace (nQubits : Int, givenU : (Qubit[] => Unit), expectedU : (Qubit[] => Unit is Adj)) : Unit
```


## <a name="input"></a>Eingabe

### <a name="nqubits--int"></a>nqubits: [int](xref:microsoft.quantum.lang-ref.int)

Die Anzahl der Qubits $n $, an denen die Vorgänge ausgeführt werden `givenU` `expectedU` .


### <a name="givenu--qubit--unit"></a>givenu: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Einheit](xref:microsoft.quantum.lang-ref.unit) 

Der Vorgang auf $n $ Qubits, der geprüft werden soll.


### <a name="expectedu--qubit--unit-adj"></a>expectedu: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ

Verweis Vorgang auf $n $ Qubits, der mit `givenU` verglichen werden soll.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="references"></a>Referenzen

Die Basis der Zustände $ \ket {0} $, $ \ket {1} $, $ \ket{+} $ und $ \ket{i} $ ist die Chuang-Nielsen Basis, die unter [ *i. L. Chuang, M. A. Nielsen*](https://arxiv.org/abs/quant-ph/9610001)beschrieben wird.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Diagnostics. assertoperationsequalreferenziert](xref:Microsoft.Quantum.Diagnostics.AssertOperationsEqualReferenced)