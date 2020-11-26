---
uid: Microsoft.Quantum.Arrays.TupleArrayAsNestedArray
title: Tuplearrayasnetstedarray-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: TupleArrayAsNestedArray
qsharp.summary: Turns a list of 2-tuples into a nested array.
ms.openlocfilehash: c898178b6385b27f753509f0748a8b666b5066bd
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220075"
---
# <a name="tuplearrayasnestedarray-function"></a><span data-ttu-id="4bdf5-102">Tuplearrayasnetstedarray-Funktion</span><span class="sxs-lookup"><span data-stu-id="4bdf5-102">TupleArrayAsNestedArray function</span></span>

<span data-ttu-id="4bdf5-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="4bdf5-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="4bdf5-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="4bdf5-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="4bdf5-105">Wandelt eine Liste von 2 Tupeln in ein Array um.</span><span class="sxs-lookup"><span data-stu-id="4bdf5-105">Turns a list of 2-tuples into a nested array.</span></span>

```qsharp
function TupleArrayAsNestedArray<'T> (tupleList : ('T, 'T)[]) : 'T[][]
```


## <a name="input"></a><span data-ttu-id="4bdf5-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="4bdf5-106">Input</span></span>

### <a name="tuplelist--tt"></a><span data-ttu-id="4bdf5-107">tuplelist: ('t, 't) []</span><span class="sxs-lookup"><span data-stu-id="4bdf5-107">tupleList : ('T,'T)[]</span></span>

<span data-ttu-id="4bdf5-108">Liste von 2-Tupeln, die in ein Array umgewandelt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="4bdf5-108">List of 2-tuples to be turned into a nested array.</span></span>



## <a name="output--t"></a><span data-ttu-id="4bdf5-109">Ausgabe: 't [] []</span><span class="sxs-lookup"><span data-stu-id="4bdf5-109">Output : 'T[][]</span></span>

<span data-ttu-id="4bdf5-110">Ein geschachtelte Array mit einer Länge, die der tuplelist entspricht.</span><span class="sxs-lookup"><span data-stu-id="4bdf5-110">A nested array with length matching the tupleList.</span></span>

## <a name="example"></a><span data-ttu-id="4bdf5-111">Beispiel</span><span class="sxs-lookup"><span data-stu-id="4bdf5-111">Example</span></span>

```qsharp
// The following returns [[2, 3], [4, 5]]
TupleArrayAsNestedArray([(2, 3), (4, 5)]);
```

## <a name="type-parameters"></a><span data-ttu-id="4bdf5-112">Typparameter</span><span class="sxs-lookup"><span data-stu-id="4bdf5-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="4bdf5-113">GIF</span><span class="sxs-lookup"><span data-stu-id="4bdf5-113">'T</span></span>

