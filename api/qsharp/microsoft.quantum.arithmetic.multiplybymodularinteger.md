---
uid: Microsoft.Quantum.Arithmetic.MultiplyByModularInteger
title: Multiplybymodularinteger-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: MultiplyByModularInteger
qsharp.summary: Performs modular multiplication by an integer constant on a qubit register.
ms.openlocfilehash: bd4e0ad6c5bad779d9a31139690021fd9fcda210
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846495"
---
# <a name="multiplybymodularinteger-operation"></a>Multiplybymodularinteger-Vorgang

Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Führt eine modulare Multiplikation durch eine ganzzahlige Konstante in einem Qubit-Register durch.

```qsharp
operation MultiplyByModularInteger (constMultiplier : Int, modulus : Int, multiplier : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a>Beschreibung

Wir geben `modulus` $N $ und `constMultiplier` $a $ an.
Durch diesen Vorgang wird ein einheitlicher Vorgang implementiert, der von der folgenden Karte auf der Berechnungsbasis definiert wird: $ $ \begin{align} \ket{y} \mapsto \ket{(a \cdot y) \operatschmue{mod} N} \end{align} $ $ für alle $y $ zwischen $0 $ und $N-$1.

## <a name="input"></a>Eingabe

### <a name="constmultiplier--int"></a>constmultiplikator: [int](xref:microsoft.quantum.lang-ref.int)

Konstante, mit der der Multiplikator multipliziert wird. Muss eine Co-Primzahl sein, um Modulus zu geben.


### <a name="modulus--int"></a>Modulo: [int](xref:microsoft.quantum.lang-ref.int)

Der Multiplikations Vorgang wird Modulo ausgeführt `modulus` .


### <a name="multiplier--littleendian"></a>Multiplikator: [littleenddian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Die Zahl, die mit einer Konstanten multipliziert wird.
Dies ist ein Array von Qubits, das eine ganze Zahl im Little-Endian-Format codiert.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Bemerkungen

- Ein Leit Diagramm und eine Erläuterung finden Sie in Abbildung 7 auf [Seite 8 von arXiv: quant-ph/0205095v3](https://arxiv.org/pdf/quant-ph/0205095v3.pdf#page=8)
- Dieser Vorgang entspricht u ₐ in [arXiv: quant-ph/0205095v3](https://arxiv.org/pdf/quant-ph/0205095v3.pdf)