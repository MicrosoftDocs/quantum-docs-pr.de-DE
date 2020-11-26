---
uid: Microsoft.Quantum.Arithmetic.ApplyXorInPlace
title: Applyxorinplace-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyXorInPlace
qsharp.summary: Applies a bitwise-XOR operation between a classical integer and an integer represented by a register of qubits.
ms.openlocfilehash: b7fc20ac421d5cff9baa3fe05450c1564f123505
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96210112"
---
# <a name="applyxorinplace-operation"></a>Applyxorinplace-Vorgang

Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Wendet eine bitweise XOR-Operation zwischen einer klassischen Ganzzahl und einer ganzen Zahl an, die durch ein Register von Qubits dargestellt wird.

```qsharp
operation ApplyXorInPlace (value : Int, target : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a>BESCHREIBUNG

Wendet `X` Vorgänge auf Qubits in einem Little-d-Register auf der Grundlage von 1 Bits in einer ganzen Zahl an.

`value`Beachten Sie, dass eine ganze Zahl ohne Vorzeichen ist, die in codiert ist, und führen Sie `target` dann `InPlaceXorLE` einen von der folgenden Zuordnung angegebenen Vorgang aus: $ \ket{y}\rightarrow \ket{y\oplus a} $, wobei $ \oplus $ der bitweise exklusive OR-Operator ist.

## <a name="input"></a>Eingabe

### <a name="value--int"></a>Wert: [int](xref:microsoft.quantum.lang-ref.int)

Eine Ganzzahl, bei der angenommen wird, dass Sie nicht negativ ist.


### <a name="target--littleendian"></a>Ziel: [littleenddian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Ein Quantum-Register, das zum Speichern von `value` in Little-d-Codierungen verwendet wird.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)

