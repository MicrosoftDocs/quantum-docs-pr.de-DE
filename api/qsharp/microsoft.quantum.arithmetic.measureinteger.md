---
uid: Microsoft.Quantum.Arithmetic.MeasureInteger
title: Wert für "messbare Ganzzahl"
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: MeasureInteger
qsharp.summary: Measures the content of a quantum register and converts it to an integer. The measurement is performed with respect to the standard computational basis, i.e., the eigenbasis of `PauliZ`.
ms.openlocfilehash: 7cd2d93332eb168c7c2be92a3b910033ca8c10ae
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707175"
---
# <a name="measureinteger-operation"></a>Wert für "messbare Ganzzahl"

Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)

Paketen [](https://nuget.org/packages/)


Misst den Inhalt eines Quantum-Registers und konvertiert ihn in eine ganze Zahl. Die Messung erfolgt in Bezug auf die standardmäßige Berechnungsbasis, d. h. auf die eigen Basis von `PauliZ` .

```qsharp
operation MeasureInteger (target : Microsoft.Quantum.Arithmetic.LittleEndian) : Int
```


## <a name="input"></a>Eingabe

### <a name="target--littleendian"></a>Ziel: [littleenddian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Ein Quantum-Register in der Little-d-Codierung.



## <a name="output--int"></a>Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)

Eine ganze Zahl ohne Vorzeichen, die den gemessenen Wert von enthält `target` .

## <a name="remarks"></a>Hinweise

Durch diesen Vorgang wird das Eingabe Register auf den Zustand "$ \ket{00\cdots 0} $" zurückgesetzt, der für die Freigabe an einen Zielcomputer geeignet ist.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Canon. Mess reintegerbe](xref:Microsoft.Quantum.Canon.MeasureIntegerBE)