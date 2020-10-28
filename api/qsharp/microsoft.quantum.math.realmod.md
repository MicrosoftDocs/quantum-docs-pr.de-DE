---
uid: Microsoft.Quantum.Math.RealMod
title: Realmod-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: RealMod
qsharp.summary: Computes the modulus between two real numbers.
ms.openlocfilehash: 6ec799885bd2f0d35314ed727356499efbe9fcf8
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706799"
---
# <a name="realmod-function"></a>Realmod-Funktion

Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)

Paketen [](https://nuget.org/packages/)


Berechnet den Modulo zwischen zwei reellen Zahlen.

```qsharp
function RealMod (value : Double, modulo : Double, minValue : Double) : Double
```


## <a name="input"></a>Eingabe

### <a name="value--double"></a>Wert: [Double](xref:microsoft.quantum.lang-ref.double)

Eine reelle Zahl $x $, um das Modul zu übernehmen.


### <a name="modulo--double"></a>Modulo: [Double](xref:microsoft.quantum.lang-ref.double)

Eine reelle Zahl, mit der der-Wert $x $ in Bezug auf übernommen wird.


### <a name="minvalue--double"></a>MinValue: [Double](xref:microsoft.quantum.lang-ref.double)

Der kleinste Wert, der von dieser Funktion zurückgegeben werden soll.



## <a name="output--double"></a>Ausgabe: [Double](xref:microsoft.quantum.lang-ref.double)



## <a name="remarks"></a>Hinweise

Diese Funktion berechnet den tatsächlichen Modulo, indem die reelle Linie über den Einheits Kreis umschließt und dann den Winkel des Einheits Kreises für die Eingabe findet.
Die `minValue` Eingabe gibt dann effektiv an, wo der Einheits Kreis abgeschnitten werden soll.