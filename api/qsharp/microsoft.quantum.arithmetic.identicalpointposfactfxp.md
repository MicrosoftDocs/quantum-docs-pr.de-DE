---
uid: Microsoft.Quantum.Arithmetic.IdenticalPointPosFactFxP
title: Identicalpointposfaktfxp-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: IdenticalPointPosFactFxP
qsharp.summary: Assert that all fixed-point numbers in the provided array have identical point positions when counting from the least- significant bit. I.e., number of bits minus point position must be constant for all fixed-point numbers in the array.
ms.openlocfilehash: 907e270e1c3710fb346044ad7757171c6d5f568d
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96223050"
---
# <a name="identicalpointposfactfxp-function"></a>Identicalpointposfaktfxp-Funktion

Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)

Paket: [Microsoft. Quantum. Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)


Bestätigen Sie, dass alle fest Komma Zahlen im angegebenen Array identische Punktpositionen aufweisen, wenn Sie vom unwichtigsten Bit gezählt werden. Dies bedeutet, dass die Anzahl der Bits, die Minuspunkt Positionen aufweisen, für alle Festkomma Zahlen im Array konstant sein muss.

```qsharp
function IdenticalPointPosFactFxP (fixedPoints : Microsoft.Quantum.Arithmetic.FixedPoint[]) : Unit
```


## <a name="input"></a>Eingabe

### <a name="fixedpoints--fixedpoint"></a>fixedpoints: [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)[]

Array von Quantum-fixpunktzahlen, die auf Kompatibilität geprüft werden (mithilfe von Assertionen).



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)

