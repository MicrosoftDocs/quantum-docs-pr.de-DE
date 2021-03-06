---
uid: Microsoft.Quantum.Arithmetic.Carry
title: Carry-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: Carry
qsharp.summary: Implements a reversible carry gate. Given a carry-in bit encoded in qubit `carryIn` and two summand bits encoded in `summand1` and `summand2`, computes the bitwise xor of `carryIn`, `summand1` and `summand2` in the qubit `summand2` and the carry-out is xored to the qubit `carryOut`.
ms.openlocfilehash: dfb08a9a9c805c0b611ab993c9b1eb949810a7da
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843350"
---
# <a name="carry-operation"></a>Carry-Vorgang

Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Implementiert ein umkehrbares durchführen. Wenn ein in Qubit codiertes `carryIn` und zwei Summen in und codiert `summand1` `summand2` sind, berechnet das bitweise XOR von `carryIn` `summand1` und `summand2` im Qubit, `summand2` und die Überführung wird im Qubit-Element als XoReD `carryOut` festgestellt.

```qsharp
operation Carry (carryIn : Qubit, summand1 : Qubit, summand2 : Qubit, carryOut : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a>Eingabe

### <a name="carryin--qubit"></a>Carryin: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

Ein-in-Qubit.


### <a name="summand1--qubit"></a>summand1: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

Erstes Summen-und Qubit-Wert.


### <a name="summand2--qubit"></a>summand2: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

Zweites Summen-und Qubit-Wert, wird durch das untere Bit der Summe von `summand1` und ersetzt `summand2` .


### <a name="carryout--qubit"></a>carryout: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

"Qubit ausführen" ist ein XoReD mit dem höheren Bit der Summe.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)

