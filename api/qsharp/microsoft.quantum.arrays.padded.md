---
uid: Microsoft.Quantum.Arrays.Padded
title: Aufgefüllte Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Padded
qsharp.summary: Returns an array padded at with specified values up to a specified length.
ms.openlocfilehash: 2b7a80d1cf5c82a1ff52bc4aa207cfe335b40061
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220534"
---
# <a name="padded-function"></a><span data-ttu-id="bae09-102">Aufgefüllte Funktion</span><span class="sxs-lookup"><span data-stu-id="bae09-102">Padded function</span></span>

<span data-ttu-id="bae09-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="bae09-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="bae09-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="bae09-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="bae09-105">Gibt ein Array zurück, das bei mit angegebenen Werten bis zu einer angegebenen Länge aufgefüllt wird.</span><span class="sxs-lookup"><span data-stu-id="bae09-105">Returns an array padded at with specified values up to a specified length.</span></span>

```qsharp
function Padded<'T> (nElementsTotal : Int, defaultElement : 'T, inputArray : 'T[]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="bae09-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="bae09-106">Input</span></span>

### <a name="nelementstotal--int"></a><span data-ttu-id="bae09-107">nelementstotal: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="bae09-107">nElementsTotal : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="bae09-108">Die Länge des aufgefüllten Arrays.</span><span class="sxs-lookup"><span data-stu-id="bae09-108">The length of the padded array.</span></span> <span data-ttu-id="bae09-109">Wenn dies positiv ist, `inputArray` wird am Kopf aufgefüllt.</span><span class="sxs-lookup"><span data-stu-id="bae09-109">If this is positive, `inputArray` is padded at the head.</span></span> <span data-ttu-id="bae09-110">Wenn diese negative Zahl ist, `inputArray` wird am Ende aufgefüllt.</span><span class="sxs-lookup"><span data-stu-id="bae09-110">If this is negative, `inputArray` is padded at the tail.</span></span>


### <a name="defaultelement--t"></a><span data-ttu-id="bae09-111">defaultelements: 't</span><span class="sxs-lookup"><span data-stu-id="bae09-111">defaultElement : 'T</span></span>

<span data-ttu-id="bae09-112">Der Standardwert, der für Auffüll Elemente verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="bae09-112">Default value to use for padding elements.</span></span>


### <a name="inputarray--t"></a><span data-ttu-id="bae09-113">Input Array: 't []</span><span class="sxs-lookup"><span data-stu-id="bae09-113">inputArray : 'T[]</span></span>

<span data-ttu-id="bae09-114">Array, dessen Werte sich an der Spitze des Ausgabe Arrays befinden.</span><span class="sxs-lookup"><span data-stu-id="bae09-114">Array whose values are at the head of the output array.</span></span>



## <a name="output--t"></a><span data-ttu-id="bae09-115">Ausgabe: 't []</span><span class="sxs-lookup"><span data-stu-id="bae09-115">Output : 'T[]</span></span>

<span data-ttu-id="bae09-116">Ein Array `output` , das `inputArray` an der Kopfzeile mit `defaultElement` s bis zu der Länge aufgefüllt wird `output` . `nElementsTotal`</span><span class="sxs-lookup"><span data-stu-id="bae09-116">An array `output` that is the `inputArray` padded at the head with `defaultElement`s until `output` has length `nElementsTotal`</span></span>

## <a name="type-parameters"></a><span data-ttu-id="bae09-117">Typparameter</span><span class="sxs-lookup"><span data-stu-id="bae09-117">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="bae09-118">GIF</span><span class="sxs-lookup"><span data-stu-id="bae09-118">'T</span></span>

<span data-ttu-id="bae09-119">Der Typ der Arrayelemente.</span><span class="sxs-lookup"><span data-stu-id="bae09-119">The type of the array elements.</span></span>