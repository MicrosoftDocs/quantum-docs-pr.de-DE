---
uid: Microsoft.Quantum.Math.RealMod
title: Realmod-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: RealMod
qsharp.summary: Computes the modulus between two real numbers.
ms.openlocfilehash: 20916d8462288395384aa875bfae4f042ba6b6ad
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96228252"
---
# <a name="realmod-function"></a>Realmod-Funktion

Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


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



## <a name="remarks"></a>Bemerkungen

Diese Funktion berechnet den tatsächlichen Modulo, indem die reelle Linie über den Einheits Kreis umschließt und dann den Winkel des Einheits Kreises für die Eingabe findet.
Die `minValue` Eingabe gibt dann effektiv an, wo der Einheits Kreis abgeschnitten werden soll.