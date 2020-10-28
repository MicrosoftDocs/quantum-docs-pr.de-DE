---
uid: Microsoft.Quantum.Arrays.LookupFunction
title: Lookupfunction-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: LookupFunction
qsharp.summary: Given an array, returns a function which returns elements of that array.
ms.openlocfilehash: c929054b96ee499db896cacf0e3ae4da6f6c4b98
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705911"
---
# <a name="lookupfunction-function"></a><span data-ttu-id="18d31-102">Lookupfunction-Funktion</span><span class="sxs-lookup"><span data-stu-id="18d31-102">LookupFunction function</span></span>

<span data-ttu-id="18d31-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="18d31-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="18d31-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="18d31-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="18d31-105">Gibt bei Angabe eines Arrays eine Funktion zurück, die Elemente dieses Arrays zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="18d31-105">Given an array, returns a function which returns elements of that array.</span></span>

```qsharp
function LookupFunction<'T> (array : 'T[]) : (Int -> 'T)
```


## <a name="input"></a><span data-ttu-id="18d31-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="18d31-106">Input</span></span>

### <a name="array--t"></a><span data-ttu-id="18d31-107">Array: 't []</span><span class="sxs-lookup"><span data-stu-id="18d31-107">array : 'T[]</span></span>

<span data-ttu-id="18d31-108">Das Array, das als Suchfunktion dargestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="18d31-108">The array to be represented as a lookup function.</span></span>



## <a name="output--int---t"></a><span data-ttu-id="18d31-109">Ausgabe: [int](xref:microsoft.quantum.lang-ref.int) -> 't</span><span class="sxs-lookup"><span data-stu-id="18d31-109">Output : [Int](xref:microsoft.quantum.lang-ref.int) -> 'T</span></span>

<span data-ttu-id="18d31-110">Eine Funktion `f` , die ist `f(idx) == f[idx]` .</span><span class="sxs-lookup"><span data-stu-id="18d31-110">A function `f` such that `f(idx) == f[idx]`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="18d31-111">Typparameter</span><span class="sxs-lookup"><span data-stu-id="18d31-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="18d31-112">GIF</span><span class="sxs-lookup"><span data-stu-id="18d31-112">'T</span></span>

<span data-ttu-id="18d31-113">Der Typ der Elemente des Arrays, das als Suchfunktion dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="18d31-113">The type of the elements of the array being represented as a lookup function.</span></span>

## <a name="remarks"></a><span data-ttu-id="18d31-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="18d31-114">Remarks</span></span>

<span data-ttu-id="18d31-115">Diese Funktion ist besonders nützlich für die Interaktion mit Funktionen und Vorgängen, die `Int -> 'T` Funktionen als Argumente annehmen.</span><span class="sxs-lookup"><span data-stu-id="18d31-115">This function is mainly useful for interoperating with functions and operations that take `Int -> 'T` functions as their arguments.</span></span> <span data-ttu-id="18d31-116">Dies ist beispielsweise in der Generator-Darstellungs Bibliothek üblich, in der Funktionen verwendet werden, um zu vermeiden, dass ein gesamtes Array im Arbeitsspeicher aufgezeichnet werden muss.</span><span class="sxs-lookup"><span data-stu-id="18d31-116">This is common, for instance, in the generator representation library, where functions are used to avoid the need to record an entire array in memory.</span></span>