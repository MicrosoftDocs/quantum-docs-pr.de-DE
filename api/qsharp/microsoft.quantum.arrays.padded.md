---
uid: Microsoft.Quantum.Arrays.Padded
title: Aufgefüllte Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Padded
qsharp.summary: Returns an array padded at with specified values up to a specified length.
ms.openlocfilehash: 556e5f5175ee54470a99f32c037eeb2cd80588d0
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845560"
---
# <a name="padded-function"></a><span data-ttu-id="08190-102">Aufgefüllte Funktion</span><span class="sxs-lookup"><span data-stu-id="08190-102">Padded function</span></span>

<span data-ttu-id="08190-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="08190-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="08190-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="08190-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="08190-105">Gibt ein Array zurück, das bei mit angegebenen Werten bis zu einer angegebenen Länge aufgefüllt wird.</span><span class="sxs-lookup"><span data-stu-id="08190-105">Returns an array padded at with specified values up to a specified length.</span></span>

```qsharp
function Padded<'T> (nElementsTotal : Int, defaultElement : 'T, inputArray : 'T[]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="08190-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="08190-106">Input</span></span>

### <a name="nelementstotal--int"></a><span data-ttu-id="08190-107">nelementstotal: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="08190-107">nElementsTotal : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="08190-108">Die Länge des aufgefüllten Arrays.</span><span class="sxs-lookup"><span data-stu-id="08190-108">The length of the padded array.</span></span> <span data-ttu-id="08190-109">Wenn dies positiv ist, `inputArray` wird am Kopf aufgefüllt.</span><span class="sxs-lookup"><span data-stu-id="08190-109">If this is positive, `inputArray` is padded at the head.</span></span> <span data-ttu-id="08190-110">Wenn diese negative Zahl ist, `inputArray` wird am Ende aufgefüllt.</span><span class="sxs-lookup"><span data-stu-id="08190-110">If this is negative, `inputArray` is padded at the tail.</span></span>


### <a name="defaultelement--t"></a><span data-ttu-id="08190-111">defaultelements: 't</span><span class="sxs-lookup"><span data-stu-id="08190-111">defaultElement : 'T</span></span>

<span data-ttu-id="08190-112">Der Standardwert, der für Auffüll Elemente verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="08190-112">Default value to use for padding elements.</span></span>


### <a name="inputarray--t"></a><span data-ttu-id="08190-113">Input Array: 't []</span><span class="sxs-lookup"><span data-stu-id="08190-113">inputArray : 'T[]</span></span>

<span data-ttu-id="08190-114">Array, dessen Werte sich an der Spitze des Ausgabe Arrays befinden.</span><span class="sxs-lookup"><span data-stu-id="08190-114">Array whose values are at the head of the output array.</span></span>



## <a name="output--t"></a><span data-ttu-id="08190-115">Ausgabe: 't []</span><span class="sxs-lookup"><span data-stu-id="08190-115">Output : 'T[]</span></span>

<span data-ttu-id="08190-116">Ein Array `output` , das `inputArray` an der Kopfzeile mit `defaultElement` s bis zu der Länge aufgefüllt wird `output` . `nElementsTotal`</span><span class="sxs-lookup"><span data-stu-id="08190-116">An array `output` that is the `inputArray` padded at the head with `defaultElement`s until `output` has length `nElementsTotal`</span></span>

## <a name="type-parameters"></a><span data-ttu-id="08190-117">Typparameter</span><span class="sxs-lookup"><span data-stu-id="08190-117">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="08190-118">GIF</span><span class="sxs-lookup"><span data-stu-id="08190-118">'T</span></span>

<span data-ttu-id="08190-119">Der Typ der Arrayelemente.</span><span class="sxs-lookup"><span data-stu-id="08190-119">The type of the array elements.</span></span>

## <a name="example"></a><span data-ttu-id="08190-120">Beispiel</span><span class="sxs-lookup"><span data-stu-id="08190-120">Example</span></span>

```qsharp
let array = [10, 11, 12];
// The following line returns [10, 12, 15, 2, 2, 2].
let output = Padded(-6, array, 2);
// The following line returns [2, 2, 2, 10, 12, 15].
let output = Padded(6, array, 2);
```