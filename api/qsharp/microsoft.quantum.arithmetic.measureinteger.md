---
uid: Microsoft.Quantum.Arithmetic.MeasureInteger
title: Wert für "messbare Ganzzahl"
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: MeasureInteger
qsharp.summary: Measures the content of a quantum register and converts it to an integer. The measurement is performed with respect to the standard computational basis, i.e., the eigenbasis of `PauliZ`.
ms.openlocfilehash: 288aee24e0ae6425db35312b560630a6bb9bfc80
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843123"
---
# <a name="measureinteger-operation"></a>Wert für "messbare Ganzzahl"

Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Misst den Inhalt eines Quantum-Registers und konvertiert ihn in eine ganze Zahl. Die Messung erfolgt in Bezug auf die standardmäßige Berechnungsbasis, d. h. auf die eigen Basis von `PauliZ` .

```qsharp
operation MeasureInteger (target : Microsoft.Quantum.Arithmetic.LittleEndian) : Int
```


## <a name="input"></a>Eingabe

### <a name="target--littleendian"></a>Ziel: [littleenddian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Ein Quantum-Register in der Little-d-Codierung.



## <a name="output--int"></a>Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)

Eine ganze Zahl ohne Vorzeichen, die den gemessenen Wert von enthält `target` .

## <a name="remarks"></a>Bemerkungen

Durch diesen Vorgang wird das Eingabe Register auf den Zustand "$ \ket{00\cdots 0} $" zurückgesetzt, der für die Freigabe an einen Zielcomputer geeignet ist.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Canon. Mess reintegerbe](xref:Microsoft.Quantum.Canon.MeasureIntegerBE)