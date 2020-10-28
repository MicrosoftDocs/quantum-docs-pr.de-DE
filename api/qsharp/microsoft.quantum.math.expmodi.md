---
uid: Microsoft.Quantum.Math.ExpModI
title: Expmodi-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ExpModI
qsharp.summary: Returns an integer raised to a given power, with respect to a given modulus.
ms.openlocfilehash: e31273702a9850d0162f160ca412ff6d50f38b28
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92723367"
---
# <a name="expmodi-function"></a>Expmodi-Funktion

Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)

Paketen [](https://nuget.org/packages/)


Gibt eine ganze Zahl zurück, die in Bezug auf einen angegebenen Modulus zu einer gegebenen Potenz ausgelöst wird.

```qsharp
function ExpModI (expBase : Int, power : Int, modulus : Int) : Int
```


## <a name="description"></a>BESCHREIBUNG

Wir bezeichnen expbase durch $x $, Power by $p $ und Modulo um $N $.
Die Funktion gibt $x ^ p \operatschmue{mod} N $ zurück.

Wir gehen davon aus, dass $N $, $x $ positiv und die Stromversorgung nicht negativ ist.

## <a name="input"></a>Eingabe

### <a name="expbase--int"></a>expbase: [int](xref:microsoft.quantum.lang-ref.int)




### <a name="power--int"></a>Power: [int](xref:microsoft.quantum.lang-ref.int)




### <a name="modulus--int"></a>Modulo: [int](xref:microsoft.quantum.lang-ref.int)





## <a name="output--int"></a>Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)



## <a name="remarks"></a>Hinweise

Nimmt Zeit proportional zur Anzahl der Bits in `power` , nicht an `power` sich selbst.