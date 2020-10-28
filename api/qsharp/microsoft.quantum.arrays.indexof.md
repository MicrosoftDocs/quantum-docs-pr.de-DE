---
uid: Microsoft.Quantum.Arrays.IndexOf
title: IndexOf-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: IndexOf
qsharp.summary: Returns the first index of the first element in an array that satisfies a given predicate. If no such element exists, returns -1.
ms.openlocfilehash: 7ff80f13f432a18f216b2dee4bd65b1e82034fa5
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705978"
---
# <a name="indexof-function"></a><span data-ttu-id="5454a-102">IndexOf-Funktion</span><span class="sxs-lookup"><span data-stu-id="5454a-102">IndexOf function</span></span>

<span data-ttu-id="5454a-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="5454a-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="5454a-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="5454a-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="5454a-105">Gibt den ersten Index des ersten Elements in einem Array zurück, das ein angegebenes Prädikat erfüllt.</span><span class="sxs-lookup"><span data-stu-id="5454a-105">Returns the first index of the first element in an array that satisfies a given predicate.</span></span> <span data-ttu-id="5454a-106">Wenn kein solches Element vorhanden ist, wird-1 zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5454a-106">If no such element exists, returns -1.</span></span>

```qsharp
function IndexOf<'T> (predicate : ('T -> Bool), arr : 'T[]) : Int
```


## <a name="input"></a><span data-ttu-id="5454a-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5454a-107">Input</span></span>

### <a name="predicate--t---bool"></a><span data-ttu-id="5454a-108">Prädikat: 't-> [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="5454a-108">predicate : 'T -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="5454a-109">Eine Prädikat Funktion, die für Elemente des Arrays fungiert.</span><span class="sxs-lookup"><span data-stu-id="5454a-109">A predicate function acting on elements of the array.</span></span>


### <a name="arr--t"></a><span data-ttu-id="5454a-110">Arr: 't []</span><span class="sxs-lookup"><span data-stu-id="5454a-110">arr : 'T[]</span></span>

<span data-ttu-id="5454a-111">Ein Array, das mithilfe des angegebenen Prädikats durchsucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="5454a-111">An array to be searched using the given predicate.</span></span>



## <a name="output--int"></a><span data-ttu-id="5454a-112">Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="5454a-112">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="5454a-113">Entweder der kleinste Index `idx` , der `predicate(arr[idx])` true ist, oder-1, wenn kein solches Element vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="5454a-113">Either the smallest index `idx` such that `predicate(arr[idx])` is true, or -1 if no such element exists.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="5454a-114">Typparameter</span><span class="sxs-lookup"><span data-stu-id="5454a-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="5454a-115">GIF</span><span class="sxs-lookup"><span data-stu-id="5454a-115">'T</span></span>

