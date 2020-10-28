---
uid: Microsoft.Quantum.Arrays.TupleArrayAsNestedArray
title: Tuplearrayasnetstedarray-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: TupleArrayAsNestedArray
qsharp.summary: Turns a list of 2-tuples into a nested array.
ms.openlocfilehash: 917f35db949790ab3ae6e7a2184bcfcf5ed50be6
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705735"
---
# <a name="tuplearrayasnestedarray-function"></a><span data-ttu-id="6c025-102">Tuplearrayasnetstedarray-Funktion</span><span class="sxs-lookup"><span data-stu-id="6c025-102">TupleArrayAsNestedArray function</span></span>

<span data-ttu-id="6c025-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="6c025-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="6c025-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="6c025-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="6c025-105">Wandelt eine Liste von 2 Tupeln in ein Array um.</span><span class="sxs-lookup"><span data-stu-id="6c025-105">Turns a list of 2-tuples into a nested array.</span></span>

```qsharp
function TupleArrayAsNestedArray<'T> (tupleList : ('T, 'T)[]) : 'T[][]
```


## <a name="input"></a><span data-ttu-id="6c025-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6c025-106">Input</span></span>

### <a name="tuplelist--tt"></a><span data-ttu-id="6c025-107">tuplelist: ('t, 't) []</span><span class="sxs-lookup"><span data-stu-id="6c025-107">tupleList : ('T,'T)[]</span></span>

<span data-ttu-id="6c025-108">Liste von 2-Tupeln, die in ein Array umgewandelt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="6c025-108">List of 2-tuples to be turned into a nested array.</span></span>



## <a name="output--t"></a><span data-ttu-id="6c025-109">Ausgabe: 't [] []</span><span class="sxs-lookup"><span data-stu-id="6c025-109">Output : 'T[][]</span></span>

<span data-ttu-id="6c025-110">Ein geschachtelte Array mit einer Länge, die der tuplelist entspricht.</span><span class="sxs-lookup"><span data-stu-id="6c025-110">A nested array with length matching the tupleList.</span></span>

## <a name="example"></a><span data-ttu-id="6c025-111">Beispiel</span><span class="sxs-lookup"><span data-stu-id="6c025-111">Example</span></span>

```qsharp
// The following returns [[2, 3], [4, 5]]
TupleArrayAsNestedArray([(2, 3), (4, 5)]);
```

## <a name="type-parameters"></a><span data-ttu-id="6c025-112">Typparameter</span><span class="sxs-lookup"><span data-stu-id="6c025-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="6c025-113">GIF</span><span class="sxs-lookup"><span data-stu-id="6c025-113">'T</span></span>

