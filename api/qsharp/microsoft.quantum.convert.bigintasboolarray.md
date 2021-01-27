---
uid: Microsoft.Quantum.Convert.BigIntAsBoolArray
title: Bigintasboolarray-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: BigIntAsBoolArray
qsharp.summary: Converts a given big integer to an array of Booleans. The 0 element of the array is the least significant bit of the big integer.
ms.openlocfilehash: 1ce83389f2ac3ce9ab2898f9d167941ca2973508
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98834592"
---
# <a name="bigintasboolarray-function"></a><span data-ttu-id="f4c17-102">Bigintasboolarray-Funktion</span><span class="sxs-lookup"><span data-stu-id="f4c17-102">BigIntAsBoolArray function</span></span>

<span data-ttu-id="f4c17-103">Namespace: [Microsoft. Quantum. Convert](xref:Microsoft.Quantum.Convert)</span><span class="sxs-lookup"><span data-stu-id="f4c17-103">Namespace: [Microsoft.Quantum.Convert](xref:Microsoft.Quantum.Convert)</span></span>

<span data-ttu-id="f4c17-104">Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="f4c17-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="f4c17-105">Konvertiert eine angegebene große Ganzzahl in ein Array von booleschen Werten.</span><span class="sxs-lookup"><span data-stu-id="f4c17-105">Converts a given big integer to an array of Booleans.</span></span>
<span data-ttu-id="f4c17-106">Das 0-Element des Arrays ist das am wenigsten bedeutende Bit der großen Ganzzahl.</span><span class="sxs-lookup"><span data-stu-id="f4c17-106">The 0 element of the array is the least significant bit of the big integer.</span></span>

```qsharp
function BigIntAsBoolArray (a : BigInt) : Bool[]
```


## <a name="input"></a><span data-ttu-id="f4c17-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f4c17-107">Input</span></span>

### <a name="a--bigint"></a><span data-ttu-id="f4c17-108">a: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="f4c17-108">a : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>





## <a name="output--bool"></a><span data-ttu-id="f4c17-109">Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)[]</span><span class="sxs-lookup"><span data-stu-id="f4c17-109">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span></span>



## <a name="remarks"></a><span data-ttu-id="f4c17-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f4c17-110">Remarks</span></span>

<span data-ttu-id="f4c17-111">Weitere Informationen finden Sie unter [c# BigInteger-Konstruktor](https://docs.microsoft.com/dotnet/api/system.numerics.biginteger.-ctor?view=netframework-4.7.2#System_Numerics_BigInteger__ctor_System_Int64_) .</span><span class="sxs-lookup"><span data-stu-id="f4c17-111">See [C# BigInteger constructor](https://docs.microsoft.com/dotnet/api/system.numerics.biginteger.-ctor?view=netframework-4.7.2#System_Numerics_BigInteger__ctor_System_Int64_) for more details.</span></span>