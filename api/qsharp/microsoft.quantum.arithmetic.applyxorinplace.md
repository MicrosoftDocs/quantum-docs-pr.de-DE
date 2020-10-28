---
uid: Microsoft.Quantum.Arithmetic.ApplyXorInPlace
title: Applyxorinplace-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyXorInPlace
qsharp.summary: Applies a bitwise-XOR operation between a classical integer and an integer represented by a register of qubits.
ms.openlocfilehash: 5a35abc16a967e64c84466a47844ed7beeb618dc
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707458"
---
# <a name="applyxorinplace-operation"></a>Applyxorinplace-Vorgang

Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)

Paketen [](https://nuget.org/packages/)


Wendet eine bitweise XOR-Operation zwischen einer klassischen Ganzzahl und einer ganzen Zahl an, die durch ein Register von Qubits dargestellt wird.

```qsharp
operation ApplyXorInPlace (value : Int, target : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
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

