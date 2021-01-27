---
uid: Microsoft.Quantum.Preparation.PrepareUniformSuperposition
title: Prepareuniforsuperposition-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PrepareUniformSuperposition
qsharp.summary: >-
  Creates a uniform superposition over states that encode 0 through `nIndices - 1`.

  That is, this unitary $U$ creates a uniform superposition over all number states $0$ to $M-1$, given an input state $\ket{0\cdots 0}$. In other words, $$ \begin{align} U\ket{0}=\frac{1}{\sqrt{M}}\sum_{j=0}^{M-1}\ket{j}. \end{align} $$.
ms.openlocfilehash: dc9d4ce1638b397748cafaa757241ce78633c67c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854321"
---
# <a name="prepareuniformsuperposition-operation"></a>Prepareuniforsuperposition-Vorgang

Namespace: [Microsoft. Quantum. Preparation](xref:Microsoft.Quantum.Preparation)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Erstellt eine einheitliche Superposition über Zustände, die 0 bis codieren `nIndices - 1` .

Das heißt, dieser einheitliche $U $ erstellt eine einheitliche Superposition für alle Zahl Zustände $0 $ bis $M-$1, wenn ein Eingabe Status $ \ket{0\cdots 0} $ angegeben wird. Anders ausgedrückt: $ $ \begin{align} u\ket {0} = \frac {1} {\sqrt{m}}\ sum_ {j = 0} ^ {M-1} \ket{j}.
\end{align} $ $.

```qsharp
operation PrepareUniformSuperposition (nIndices : Int, indexRegister : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="input"></a>Eingabe

### <a name="nindices--int"></a>nindizes: [int](xref:microsoft.quantum.lang-ref.int)

Die gewünschte Anzahl von Zuständen $M $ in der einheitlichen Superposition.


### <a name="indexregister--littleendian"></a>Indexregister: [littleerdian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Das Qubit-Register, das die Zahlen Zustände im- `LittleEndian` Format speichert.
Dieses Register muss in der Lage sein, die Zahl $M-$1 zu speichern, und es wird davon ausgegangen, dass es im Status $ \ket{0\cdots 0} $ initialisiert wird.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="example"></a>Beispiel

Im folgenden Beispiel wird der Status $ \frac {1} {\sqrt {6} } \ sum_ {j = 0} ^ {5} \ket{j} $ auf $3 $ Qubits vorbereitet.

```qsharp
let nIndices = 6;
using(indexRegister = Qubit[3]) {
    PrepareUniformSuperposition(nIndices, LittleEndian(indexRegister));
    // ...
}
```

## <a name="remarks"></a>Bemerkungen

Der Vorgang ist "adjointable", erfordert jedoch, dass `indexRegister` sich in diesem Fall in einer einheitlichen übergeordneten Position befindet `nIndices` .