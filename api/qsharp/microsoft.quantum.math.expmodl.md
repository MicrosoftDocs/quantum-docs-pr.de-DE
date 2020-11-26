---
uid: Microsoft.Quantum.Math.ExpModL
title: Expmodl-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ExpModL
qsharp.summary: Returns an integer raised to a given power, with respect to a given modulus.
ms.openlocfilehash: 07da113caeb9f6f3f3f3f92f13478f33021bfa14
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96210744"
---
# <a name="expmodl-function"></a>Expmodl-Funktion

Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


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



## <a name="remarks"></a>Bemerkungen

Nimmt Zeit proportional zur Anzahl der Bits in `power` , nicht an `power` sich selbst.