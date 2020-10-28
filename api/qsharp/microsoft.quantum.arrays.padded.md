---
uid: Microsoft.Quantum.Arrays.Padded
title: Aufgefüllte Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Padded
qsharp.summary: Returns an array padded at with specified values up to a specified length.
ms.openlocfilehash: 8742d4726e7ee32349bf3d0bd5077352ffca350b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705850"
---
# <a name="padded-function"></a><span data-ttu-id="3b2ec-102">Aufgefüllte Funktion</span><span class="sxs-lookup"><span data-stu-id="3b2ec-102">Padded function</span></span>

<span data-ttu-id="3b2ec-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="3b2ec-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="3b2ec-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="3b2ec-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="3b2ec-105">Gibt ein Array zurück, das bei mit angegebenen Werten bis zu einer angegebenen Länge aufgefüllt wird.</span><span class="sxs-lookup"><span data-stu-id="3b2ec-105">Returns an array padded at with specified values up to a specified length.</span></span>

```qsharp
function Padded<'T> (nElementsTotal : Int, defaultElement : 'T, inputArray : 'T[]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="3b2ec-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="3b2ec-106">Input</span></span>

### <a name="nelementstotal--int"></a><span data-ttu-id="3b2ec-107">nelementstotal: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="3b2ec-107">nElementsTotal : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="3b2ec-108">Die Länge des aufgefüllten Arrays.</span><span class="sxs-lookup"><span data-stu-id="3b2ec-108">The length of the padded array.</span></span> <span data-ttu-id="3b2ec-109">Wenn dies positiv ist, `inputArray` wird am Kopf aufgefüllt.</span><span class="sxs-lookup"><span data-stu-id="3b2ec-109">If this is positive, `inputArray` is padded at the head.</span></span> <span data-ttu-id="3b2ec-110">Wenn diese negative Zahl ist, `inputArray` wird am Ende aufgefüllt.</span><span class="sxs-lookup"><span data-stu-id="3b2ec-110">If this is negative, `inputArray` is padded at the tail.</span></span>


### <a name="defaultelement--t"></a><span data-ttu-id="3b2ec-111">defaultelements: 't</span><span class="sxs-lookup"><span data-stu-id="3b2ec-111">defaultElement : 'T</span></span>

<span data-ttu-id="3b2ec-112">Der Standardwert, der für Auffüll Elemente verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="3b2ec-112">Default value to use for padding elements.</span></span>


### <a name="inputarray--t"></a><span data-ttu-id="3b2ec-113">Input Array: 't []</span><span class="sxs-lookup"><span data-stu-id="3b2ec-113">inputArray : 'T[]</span></span>

<span data-ttu-id="3b2ec-114">Array, dessen Werte sich an der Spitze des Ausgabe Arrays befinden.</span><span class="sxs-lookup"><span data-stu-id="3b2ec-114">Array whose values are at the head of the output array.</span></span>



## <a name="output--t"></a><span data-ttu-id="3b2ec-115">Ausgabe: 't []</span><span class="sxs-lookup"><span data-stu-id="3b2ec-115">Output : 'T[]</span></span>

<span data-ttu-id="3b2ec-116">Ein Array `output` , das `inputArray` an der Kopfzeile mit `defaultElement` s bis zu der Länge aufgefüllt wird `output` . `nElementsTotal`</span><span class="sxs-lookup"><span data-stu-id="3b2ec-116">An array `output` that is the `inputArray` padded at the head with `defaultElement`s until `output` has length `nElementsTotal`</span></span>

## <a name="type-parameters"></a><span data-ttu-id="3b2ec-117">Typparameter</span><span class="sxs-lookup"><span data-stu-id="3b2ec-117">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="3b2ec-118">GIF</span><span class="sxs-lookup"><span data-stu-id="3b2ec-118">'T</span></span>

<span data-ttu-id="3b2ec-119">Der Typ der Arrayelemente.</span><span class="sxs-lookup"><span data-stu-id="3b2ec-119">The type of the array elements.</span></span>