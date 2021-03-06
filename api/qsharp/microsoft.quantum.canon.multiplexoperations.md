---
uid: Microsoft.Quantum.Canon.MultiplexOperations
title: Multiplexoperations-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: MultiplexOperations
qsharp.summary: >-
  Applies an array of operations controlled by an array of number states.

  That is, applies Multiply-controlled unitary operation $U$ that applies a unitary $V_j$ when controlled by $n$-qubit number state $\ket{j}$.

  $U = \sum^{2^n-1}_{j=0}\ket{j}\bra{j}\otimes V_j$.
ms.openlocfilehash: 1cf483bb0d3b7cc43d271b65a2363fab95ff0f3b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98852525"
---
# <a name="multiplexoperations-operation"></a>Multiplexoperations-Vorgang

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Wendet ein Array von Vorgängen an, die von einem Array von Zahlen Zuständen gesteuert werden.

Das heißt, dass der mehrfach gesteuerte einheitliche Vorgang $U $ angewendet wird, der eine einheitliche $V _J $ anwendet, wenn dies durch $n $-Qubit-Zahlen Status $ \ket{j} $ gesteuert wird.

$U = \sum ^ {2 ^ n-1} _ {j = 0} \ket{j}\bra{j}\otimes V_j $.

```qsharp
operation MultiplexOperations<'T> (unitaries : ('T => Unit is Adj + Ctl)[], index : Microsoft.Quantum.Arithmetic.LittleEndian, target : 'T) : Unit is Adj + Ctl
```


## <a name="input"></a>Eingabe

### <a name="unitaries--t--unit--is-adj--ctl"></a>Uni-Zuflüsse: 't => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL []

Array von bis zu $2 ^ n $ einheitlichen Vorgängen. Der $j $ Th-Vorgang wird durch den Zahlen Status $ \ket{j} $ codiert, der im Little-Endian-Format codiert ist.


### <a name="index--littleendian"></a>Index: [littleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

$n $-Qubit-Steuerelement Register, das die Anzahl der Zustände $ \ket{j} $ im Little-Endian-Format codiert.


### <a name="target--t"></a>Ziel: 't

Generisches Qubit-Register, für das $V _J $ agiert.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Typparameter

### <a name="t"></a>GIF



## <a name="remarks"></a>Bemerkungen

`coefficients` wird mit Identitäts Elementen aufgefüllt, wenn weniger als $2 ^ n $ angegeben werden. Diese Implementierung verwendet $n-$1-hilfssbits.

## <a name="references"></a>References

- Zur ersten Quantum-Simulation mit Quantum Beschleunigung Andrew M. Childs, Dmitri Maslov, yunabong Nam, Neil J. Ross, Yuan su https://arxiv.org/abs/1711.10980