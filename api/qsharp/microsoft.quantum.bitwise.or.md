---
uid: Microsoft.Quantum.Bitwise.Or
title: Or-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Bitwise
qsharp.name: Or
qsharp.summary: Returns the bitwise OR of two integers. This performs the same computation as the built-in `|||` operator.
ms.openlocfilehash: 811e7cf64424e8302c5745c4c71d76de50ab8c08
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845278"
---
# <a name="or-function"></a><span data-ttu-id="6330d-102">Or-Funktion</span><span class="sxs-lookup"><span data-stu-id="6330d-102">Or function</span></span>

<span data-ttu-id="6330d-103">Namespace: [Microsoft. Quantum. bitse](xref:Microsoft.Quantum.Bitwise)</span><span class="sxs-lookup"><span data-stu-id="6330d-103">Namespace: [Microsoft.Quantum.Bitwise](xref:Microsoft.Quantum.Bitwise)</span></span>

<span data-ttu-id="6330d-104">Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="6330d-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="6330d-105">Gibt das bitweise OR von zwei Ganzzahlen zurück.</span><span class="sxs-lookup"><span data-stu-id="6330d-105">Returns the bitwise OR of two integers.</span></span>
<span data-ttu-id="6330d-106">Dies führt die gleiche Berechnung durch wie der integrierte `|||` Operator.</span><span class="sxs-lookup"><span data-stu-id="6330d-106">This performs the same computation as the built-in `|||` operator.</span></span>

```qsharp
function Or (a : Int, b : Int) : Int
```


## <a name="input"></a><span data-ttu-id="6330d-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6330d-107">Input</span></span>

### <a name="a--int"></a><span data-ttu-id="6330d-108">a: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="6330d-108">a : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>




### <a name="b--int"></a><span data-ttu-id="6330d-109">b: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="6330d-109">b : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>





## <a name="output--int"></a><span data-ttu-id="6330d-110">Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="6330d-110">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>



## <a name="example"></a><span data-ttu-id="6330d-111">Beispiel</span><span class="sxs-lookup"><span data-stu-id="6330d-111">Example</span></span>

```qsharp
let a = 248;      //                 11111000₂
let b = 63;       //                 00111111₂
let x = Or(a, b); // x : Int = 255 = 11111111₂.
```

## <a name="remarks"></a><span data-ttu-id="6330d-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6330d-112">Remarks</span></span>

<span data-ttu-id="6330d-113">Weitere Informationen finden Sie unter [c# | -Operator](https://docs.microsoft.com/dotnet/csharp/language-reference/operators/or-operator) , um weitere Details anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="6330d-113">See the [C# | Operator](https://docs.microsoft.com/dotnet/csharp/language-reference/operators/or-operator) for more details.</span></span>