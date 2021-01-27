---
uid: Microsoft.Quantum.Math.RealMod
title: Realmod-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: RealMod
qsharp.summary: Computes the modulus between two real numbers.
ms.openlocfilehash: 56da313fabb20655ec358120b8d9b435e4971159
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848344"
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



## <a name="example"></a>Beispiel

```qsharp
    // Returns 3 π / 2.
    let y = RealMod(5.5 * PI(), 2.0 * PI(), 0.0);
    // Returns -1.2, since +3.6 and -1.2 are 4.8 apart on the real line,
    // which is a multiple of 2.4.
    let z = RealMod(3.6, 2.4, -1.2);
```

## <a name="remarks"></a>Bemerkungen

Diese Funktion berechnet den tatsächlichen Modulo, indem die reelle Linie über den Einheits Kreis umschließt und dann den Winkel des Einheits Kreises für die Eingabe findet.
Die `minValue` Eingabe gibt dann effektiv an, wo der Einheits Kreis abgeschnitten werden soll.