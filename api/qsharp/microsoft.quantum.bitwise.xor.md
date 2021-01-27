---
uid: Microsoft.Quantum.Bitwise.Xor
title: XOR-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Bitwise
qsharp.name: Xor
qsharp.summary: Returns the bitwise exclusive-OR (XOR) of two integers. This performs the same computation as the built-in `^^^` operator.
ms.openlocfilehash: ac31ba973ff06424dbd16168dac14a79b2691b3f
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842077"
---
# <a name="xor-function"></a><span data-ttu-id="4a0b1-102">XOR-Funktion</span><span class="sxs-lookup"><span data-stu-id="4a0b1-102">Xor function</span></span>

<span data-ttu-id="4a0b1-103">Namespace: [Microsoft. Quantum. bitse](xref:Microsoft.Quantum.Bitwise)</span><span class="sxs-lookup"><span data-stu-id="4a0b1-103">Namespace: [Microsoft.Quantum.Bitwise](xref:Microsoft.Quantum.Bitwise)</span></span>

<span data-ttu-id="4a0b1-104">Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="4a0b1-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="4a0b1-105">Gibt das bitweise exklusive OR (XOR) zweier ganzer Zahlen zurück.</span><span class="sxs-lookup"><span data-stu-id="4a0b1-105">Returns the bitwise exclusive-OR (XOR) of two integers.</span></span>
<span data-ttu-id="4a0b1-106">Dies führt die gleiche Berechnung durch wie der integrierte `^^^` Operator.</span><span class="sxs-lookup"><span data-stu-id="4a0b1-106">This performs the same computation as the built-in `^^^` operator.</span></span>

```qsharp
function Xor (a : Int, b : Int) : Int
```


## <a name="input"></a><span data-ttu-id="4a0b1-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="4a0b1-107">Input</span></span>

### <a name="a--int"></a><span data-ttu-id="4a0b1-108">a: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="4a0b1-108">a : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>




### <a name="b--int"></a><span data-ttu-id="4a0b1-109">b: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="4a0b1-109">b : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>





## <a name="output--int"></a><span data-ttu-id="4a0b1-110">Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="4a0b1-110">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>



## <a name="example"></a><span data-ttu-id="4a0b1-111">Beispiel</span><span class="sxs-lookup"><span data-stu-id="4a0b1-111">Example</span></span>

```qsharp
let a = 248;       //                 11111000₂
let b = 63;        //                 00111111₂
let x = Xor(a, b); // x : Int = 199 = 11000111₂.
```

## <a name="remarks"></a><span data-ttu-id="4a0b1-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4a0b1-112">Remarks</span></span>

<span data-ttu-id="4a0b1-113">Weitere Informationen finden Sie unter [c# ^-Operator](https://docs.microsoft.com/dotnet/csharp/language-reference/operators/xor-operator) .</span><span class="sxs-lookup"><span data-stu-id="4a0b1-113">See the [C# ^ Operator](https://docs.microsoft.com/dotnet/csharp/language-reference/operators/xor-operator) for more details.</span></span>