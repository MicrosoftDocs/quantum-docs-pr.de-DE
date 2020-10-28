---
uid: Microsoft.Quantum.Math.ExpModL
title: Expmodl-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ExpModL
qsharp.summary: Returns an integer raised to a given power, with respect to a given modulus.
ms.openlocfilehash: 73d434bd364847b4e5e06d1a9f460424e0c50850
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92723731"
---
# <a name="expmodl-function"></a>Expmodl-Funktion

Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)

Paketen [](https://nuget.org/packages/)


Gibt eine ganze Zahl zurück, die in Bezug auf einen angegebenen Modulus zu einer gegebenen Potenz ausgelöst wird.

```qsharp
function ExpModL (expBase : BigInt, power : BigInt, modulus : BigInt) : BigInt
```


## <a name="description"></a>BESCHREIBUNG

Wir bezeichnen expbase durch $x $, Power by $p $ und Modulo um $N $.
Die Funktion gibt $x ^ p \operatschmue{mod} N $ zurück.

Wir gehen davon aus, dass $N $, $x $ positiv und die Stromversorgung nicht negativ ist.

## <a name="input"></a>Eingabe

### <a name="expbase--bigint"></a>expbase: [bigint](xref:microsoft.quantum.lang-ref.bigint)




### <a name="power--bigint"></a>Leistung: [bigint](xref:microsoft.quantum.lang-ref.bigint)




### <a name="modulus--bigint"></a>Modulo: [bigint](xref:microsoft.quantum.lang-ref.bigint)





## <a name="output--bigint"></a>Ausgabe: [bigint](xref:microsoft.quantum.lang-ref.bigint)



## <a name="remarks"></a>Hinweise

Nimmt Zeit proportional zur Anzahl der Bits in `power` , nicht an `power` sich selbst.