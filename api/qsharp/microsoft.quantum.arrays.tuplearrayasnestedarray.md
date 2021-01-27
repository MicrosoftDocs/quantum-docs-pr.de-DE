---
uid: Microsoft.Quantum.Arrays.TupleArrayAsNestedArray
title: Tuplearrayasnetstedarray-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: TupleArrayAsNestedArray
qsharp.summary: Turns a list of 2-tuples into a nested array.
ms.openlocfilehash: 51a35555080d1d2475fc1aa9e48e84c7c6f92c51
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845392"
---
# <a name="tuplearrayasnestedarray-function"></a><span data-ttu-id="864c0-102">Tuplearrayasnetstedarray-Funktion</span><span class="sxs-lookup"><span data-stu-id="864c0-102">TupleArrayAsNestedArray function</span></span>

<span data-ttu-id="864c0-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="864c0-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="864c0-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="864c0-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="864c0-105">Wandelt eine Liste von 2 Tupeln in ein Array um.</span><span class="sxs-lookup"><span data-stu-id="864c0-105">Turns a list of 2-tuples into a nested array.</span></span>

```qsharp
function TupleArrayAsNestedArray<'T> (tupleList : ('T, 'T)[]) : 'T[][]
```


## <a name="input"></a><span data-ttu-id="864c0-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="864c0-106">Input</span></span>

### <a name="tuplelist--tt"></a><span data-ttu-id="864c0-107">tuplelist: ('t, 't) []</span><span class="sxs-lookup"><span data-stu-id="864c0-107">tupleList : ('T,'T)[]</span></span>

<span data-ttu-id="864c0-108">Liste von 2-Tupeln, die in ein Array umgewandelt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="864c0-108">List of 2-tuples to be turned into a nested array.</span></span>



## <a name="output--t"></a><span data-ttu-id="864c0-109">Ausgabe: 't [] []</span><span class="sxs-lookup"><span data-stu-id="864c0-109">Output : 'T[][]</span></span>

<span data-ttu-id="864c0-110">Ein geschachtelte Array mit einer Länge, die der tuplelist entspricht.</span><span class="sxs-lookup"><span data-stu-id="864c0-110">A nested array with length matching the tupleList.</span></span>

## <a name="example"></a><span data-ttu-id="864c0-111">Beispiel</span><span class="sxs-lookup"><span data-stu-id="864c0-111">Example</span></span>

```qsharp
// The following returns [[2, 3], [4, 5]]
TupleArrayAsNestedArray([(2, 3), (4, 5)]);
```

## <a name="type-parameters"></a><span data-ttu-id="864c0-112">Typparameter</span><span class="sxs-lookup"><span data-stu-id="864c0-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="864c0-113">GIF</span><span class="sxs-lookup"><span data-stu-id="864c0-113">'T</span></span>

