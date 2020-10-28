---
uid: Microsoft.Quantum.Preparation.PrepareUniformSuperposition
title: Prepareuniforsuperposition-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PrepareUniformSuperposition
qsharp.summary: >-
  Creates a uniform superposition over states that encode 0 through `nIndices - 1`.

  That is, this unitary $U$ creates a uniform superposition over all number states $0$ to $M-1$, given an input state $\ket{0\cdots 0}$. In other words, $$ \begin{align} U\ket{0}=\frac{1}{\sqrt{M}}\sum_{j=0}^{M-1}\ket{j}. \end{align} $$.
ms.openlocfilehash: 8b57a7a02e9f704cf9677574824dfdc93fff25b0
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92701249"
---
# <a name="prepareuniformsuperposition-operation"></a>Prepareuniforsuperposition-Vorgang

Namespace: [Microsoft. Quantum. Preparation](xref:Microsoft.Quantum.Preparation)

Paketen [](https://nuget.org/packages/)


Erstellt eine einheitliche Superposition über Zustände, die 0 bis codieren `nIndices - 1` .

Das heißt, dieser einheitliche $U $ erstellt eine einheitliche Superposition für alle Zahl Zustände $0 $ bis $M-$1, wenn ein Eingabe Status $ \ket{0\cdots 0} $ angegeben wird. Anders ausgedrückt: $ $ \begin{align} u\ket {0} = \frac {1} {\sqrt{m}}\ sum_ {j = 0} ^ {M-1} \ket{j}.
\end{align} $ $.

```qsharp
operation PrepareUniformSuperposition (nIndices : Int, indexRegister : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="input"></a>Eingabe

### <a name="nindices--int"></a>nindizes: [int](xref:microsoft.quantum.lang-ref.int)

Die gewünschte Anzahl von Zuständen $M $ in der einheitlichen Superposition.


### <a name="indexregister--littleendian"></a>Indexregister: [littleerdian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Das Qubit-Register, das die Zahlen Zustände im- `LittleEndian` Format speichert.
Dieses Register muss in der Lage sein, die Zahl $M-$1 zu speichern, und es wird davon ausgegangen, dass es im Status $ \ket{0\cdots 0} $ initialisiert wird.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Hinweise

Der Vorgang ist "adjointable", erfordert jedoch, dass `indexRegister` sich in diesem Fall in einer einheitlichen übergeordneten Position befindet `nIndices` .