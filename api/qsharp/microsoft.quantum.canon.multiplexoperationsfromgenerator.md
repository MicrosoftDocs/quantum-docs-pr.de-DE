---
uid: Microsoft.Quantum.Canon.MultiplexOperationsFromGenerator
title: Multiplexoperationsfromgenerator-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: MultiplexOperationsFromGenerator
qsharp.summary: >-
  Applies a multiply-controlled unitary operation $U$ that applies a unitary $V_j$ when controlled by n-qubit number state $\ket{j}$.

  $U = \sum^{N-1}_{j=0}\ket{j}\bra{j}\otimes V_j$.
ms.openlocfilehash: 2fde0bf391568f39128e6dca4b535aa6b78407c2
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703967"
---
# <a name="multiplexoperationsfromgenerator-operation"></a>Multiplexoperationsfromgenerator-Vorgang

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paketen [](https://nuget.org/packages/)


Wendet einen mehrfach gesteuerten einheitlichen Vorgang $U $ an, der eine einheitliche $V _J $ anwendet, wenn dies durch den n-Qubit-Zahlen Status $ \ket{j} $ gesteuert wird.

$U = \sum ^ {N-1} _ {j = 0} \ket{j}\bra{j}\otimes V_j $.

```qsharp
operation MultiplexOperationsFromGenerator<'T> (unitaryGenerator : (Int, (Int -> ('T => Unit is Adj + Ctl))), index : Microsoft.Quantum.Arithmetic.LittleEndian, target : 'T) : Unit
```


## <a name="input"></a>Eingabe

### <a name="unitarygenerator--intint---t--unit-adj--ctl"></a>unitarygenerator: ([int](xref:microsoft.quantum.lang-ref.int),[int](xref:microsoft.quantum.lang-ref.int) -> 't => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL)

Ein Tupel, bei dem das erste Element `Int` die Anzahl von uniflüssen $N $ und das zweite Element `(Int -> ('T => () is Adj + Ctl))` eine Funktion ist, die eine ganze Zahl $j $ in $ [0, N-1] $ annimmt und den einheitlichen Vorgang $V _J $ ausgibt.


### <a name="index--littleendian"></a>Index: [littleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

$n $-Qubit-Steuerelement Register, das die Anzahl der Zustände $ \ket{j} $ im Little-Endian-Format codiert.


### <a name="target--t"></a>Ziel: 't

Generisches Qubit-Register, für das $V _J $ agiert.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Typparameter

### <a name="t"></a>GIF



## <a name="remarks"></a>Hinweise

`coefficients` wird mit Identitäts Elementen aufgefüllt, wenn weniger als $2 ^ n $ angegeben werden. Diese Implementierung verwendet $n-$1-hilfssbits.

## <a name="references"></a>Referenzen

- [*Andrew M. Childs, Dmitri Maslov, yunabong Nam, Neil J. Ross, Yuan su* , arXiv: 1711.10980](https://arxiv.org/abs/1711.10980)