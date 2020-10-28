---
uid: Microsoft.Quantum.Arithmetic.IdenticalPointPosFactFxP
title: Identicalpointposfaktfxp-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: IdenticalPointPosFactFxP
qsharp.summary: Assert that all fixed-point numbers in the provided array have identical point positions when counting from the least- significant bit. I.e., number of bits minus point position must be constant for all fixed-point numbers in the array.
ms.openlocfilehash: 0b285ce980ca1abbc3eb20838389a6f49835e742
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707274"
---
# <a name="identicalpointposfactfxp-function"></a>Identicalpointposfaktfxp-Funktion

Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)

Paketen [](https://nuget.org/packages/)


Bestätigen Sie, dass alle fest Komma Zahlen im angegebenen Array identische Punktpositionen aufweisen, wenn Sie vom unwichtigsten Bit gezählt werden. Dies bedeutet, dass die Anzahl der Bits, die Minuspunkt Positionen aufweisen, für alle Festkomma Zahlen im Array konstant sein muss.

```qsharp
function IdenticalPointPosFactFxP (fixedPoints : Microsoft.Quantum.Arithmetic.FixedPoint[]) : Unit
```


## <a name="input"></a>Eingabe

### <a name="fixedpoints--fixedpoint"></a>fixedpoints: [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)[]

Array von Quantum-fixpunktzahlen, die auf Kompatibilität geprüft werden (mithilfe von Assertionen).



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)

