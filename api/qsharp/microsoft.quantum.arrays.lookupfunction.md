---
uid: Microsoft.Quantum.Arrays.LookupFunction
title: Lookupfunction-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: LookupFunction
qsharp.summary: Given an array, returns a function which returns elements of that array.
ms.openlocfilehash: 22b56bb7e9f03ebc5b2225efb2e6450d56022664
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845701"
---
# <a name="lookupfunction-function"></a><span data-ttu-id="fbe63-102">Lookupfunction-Funktion</span><span class="sxs-lookup"><span data-stu-id="fbe63-102">LookupFunction function</span></span>

<span data-ttu-id="fbe63-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="fbe63-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="fbe63-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="fbe63-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="fbe63-105">Gibt bei Angabe eines Arrays eine Funktion zurück, die Elemente dieses Arrays zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="fbe63-105">Given an array, returns a function which returns elements of that array.</span></span>

```qsharp
function LookupFunction<'T> (array : 'T[]) : (Int -> 'T)
```


## <a name="input"></a><span data-ttu-id="fbe63-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="fbe63-106">Input</span></span>

### <a name="array--t"></a><span data-ttu-id="fbe63-107">Array: 't []</span><span class="sxs-lookup"><span data-stu-id="fbe63-107">array : 'T[]</span></span>

<span data-ttu-id="fbe63-108">Das Array, das als Suchfunktion dargestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="fbe63-108">The array to be represented as a lookup function.</span></span>



## <a name="output--int---t"></a><span data-ttu-id="fbe63-109">Ausgabe: [int](xref:microsoft.quantum.lang-ref.int) -> 't</span><span class="sxs-lookup"><span data-stu-id="fbe63-109">Output : [Int](xref:microsoft.quantum.lang-ref.int) -> 'T</span></span>

<span data-ttu-id="fbe63-110">Eine Funktion `f` , die ist `f(idx) == f[idx]` .</span><span class="sxs-lookup"><span data-stu-id="fbe63-110">A function `f` such that `f(idx) == f[idx]`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="fbe63-111">Typparameter</span><span class="sxs-lookup"><span data-stu-id="fbe63-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="fbe63-112">GIF</span><span class="sxs-lookup"><span data-stu-id="fbe63-112">'T</span></span>

<span data-ttu-id="fbe63-113">Der Typ der Elemente des Arrays, das als Suchfunktion dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="fbe63-113">The type of the elements of the array being represented as a lookup function.</span></span>

## <a name="remarks"></a><span data-ttu-id="fbe63-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fbe63-114">Remarks</span></span>

<span data-ttu-id="fbe63-115">Diese Funktion ist besonders nützlich für die Interaktion mit Funktionen und Vorgängen, die `Int -> 'T` Funktionen als Argumente annehmen.</span><span class="sxs-lookup"><span data-stu-id="fbe63-115">This function is mainly useful for interoperating with functions and operations that take `Int -> 'T` functions as their arguments.</span></span> <span data-ttu-id="fbe63-116">Dies ist beispielsweise in der Generator-Darstellungs Bibliothek üblich, in der Funktionen verwendet werden, um zu vermeiden, dass ein gesamtes Array im Arbeitsspeicher aufgezeichnet werden muss.</span><span class="sxs-lookup"><span data-stu-id="fbe63-116">This is common, for instance, in the generator representation library, where functions are used to avoid the need to record an entire array in memory.</span></span>