---
uid: Microsoft.Quantum.Math.ExpModL
title: Expmodl-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ExpModL
qsharp.summary: Returns an integer raised to a given power, with respect to a given modulus.
ms.openlocfilehash: 127f2e51e19c76f4f7973bf1ac2217d4fffd72f6
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848370"
---
# <a name="expmodl-function"></a>Expmodl-Funktion

Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Gibt eine ganze Zahl zurück, die in Bezug auf einen angegebenen Modulus zu einer gegebenen Potenz ausgelöst wird.

```qsharp
function ExpModL (expBase : BigInt, power : BigInt, modulus : BigInt) : BigInt
```


## <a name="description"></a>Beschreibung

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