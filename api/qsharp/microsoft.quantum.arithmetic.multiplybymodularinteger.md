---
uid: Microsoft.Quantum.Arithmetic.MultiplyByModularInteger
title: Multiplybymodularinteger-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: MultiplyByModularInteger
qsharp.summary: Performs modular multiplication by an integer constant on a qubit register.
ms.openlocfilehash: 6deced7862ab4cb74315219eaaab97380cdf0f92
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706391"
---
# <a name="multiplybymodularinteger-operation"></a>Multiplybymodularinteger-Vorgang

Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)

Paketen [](https://nuget.org/packages/)


Führt eine modulare Multiplikation durch eine ganzzahlige Konstante in einem Qubit-Register durch.

```qsharp
operation MultiplyByModularInteger (constMultiplier : Int, modulus : Int, multiplier : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="description"></a>BESCHREIBUNG

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



## <a name="remarks"></a>Hinweise

- Ein Leit Diagramm und eine Erläuterung finden Sie in Abbildung 7 auf [Seite 8 von arXiv: quant-ph/0205095v3](https://arxiv.org/pdf/quant-ph/0205095v3.pdf#page=8)
- Dieser Vorgang entspricht u ₐ in [arXiv: quant-ph/0205095v3](https://arxiv.org/pdf/quant-ph/0205095v3.pdf)