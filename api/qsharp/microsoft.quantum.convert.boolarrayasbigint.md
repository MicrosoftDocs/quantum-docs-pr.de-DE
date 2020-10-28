---
uid: Microsoft.Quantum.Convert.BoolArrayAsBigInt
title: Boolarrayasbigint-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: BoolArrayAsBigInt
qsharp.summary: Converts a given array of Booleans to an equivalent big integer. The 0 element of the array is the least significant bit of the big integer.
ms.openlocfilehash: 75656ba188a1b822eb42e98412365bf5873bf46e
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703031"
---
# <a name="boolarrayasbigint-function"></a>Boolarrayasbigint-Funktion

Namespace: [Microsoft. Quantum. Convert](xref:Microsoft.Quantum.Convert)

Paketen [](https://nuget.org/packages/)


Konvertiert ein angegebenes Array von booleschen Werten in eine entsprechende große Ganzzahl.
Das 0-Element des Arrays ist das am wenigsten bedeutende Bit der großen Ganzzahl.

```qsharp
function BoolArrayAsBigInt (a : Bool[]) : BigInt
```


## <a name="input"></a>Eingabe

### <a name="a--bool"></a>a: [bool](xref:microsoft.quantum.lang-ref.bool)[]





## <a name="output--bigint"></a>Ausgabe: [bigint](xref:microsoft.quantum.lang-ref.bigint)



## <a name="remarks"></a>Hinweise

Weitere Informationen finden Sie unter [c# BigInteger-Konstruktor](https://docs.microsoft.com/dotnet/api/system.numerics.biginteger.-ctor?view=netframework-4.7.2#System_Numerics_BigInteger__ctor_System_Int64_) .