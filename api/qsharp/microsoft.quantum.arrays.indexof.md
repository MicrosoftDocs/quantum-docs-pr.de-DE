---
uid: Microsoft.Quantum.Arrays.IndexOf
title: IndexOf-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: IndexOf
qsharp.summary: Returns the first index of the first element in an array that satisfies a given predicate. If no such element exists, returns -1.
ms.openlocfilehash: 64db55e831078a7130a3ced6a30bfbd2299c392d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848524"
---
# <a name="indexof-function"></a><span data-ttu-id="bf6de-102">IndexOf-Funktion</span><span class="sxs-lookup"><span data-stu-id="bf6de-102">IndexOf function</span></span>

<span data-ttu-id="bf6de-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="bf6de-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="bf6de-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="bf6de-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="bf6de-105">Gibt den ersten Index des ersten Elements in einem Array zurück, das ein angegebenes Prädikat erfüllt.</span><span class="sxs-lookup"><span data-stu-id="bf6de-105">Returns the first index of the first element in an array that satisfies a given predicate.</span></span> <span data-ttu-id="bf6de-106">Wenn kein solches Element vorhanden ist, wird-1 zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="bf6de-106">If no such element exists, returns -1.</span></span>

```qsharp
function IndexOf<'T> (predicate : ('T -> Bool), arr : 'T[]) : Int
```


## <a name="input"></a><span data-ttu-id="bf6de-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="bf6de-107">Input</span></span>

### <a name="predicate--t---bool"></a><span data-ttu-id="bf6de-108">Prädikat: 't-> [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="bf6de-108">predicate : 'T -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="bf6de-109">Eine Prädikat Funktion, die für Elemente des Arrays fungiert.</span><span class="sxs-lookup"><span data-stu-id="bf6de-109">A predicate function acting on elements of the array.</span></span>


### <a name="arr--t"></a><span data-ttu-id="bf6de-110">Arr: 't []</span><span class="sxs-lookup"><span data-stu-id="bf6de-110">arr : 'T[]</span></span>

<span data-ttu-id="bf6de-111">Ein Array, das mithilfe des angegebenen Prädikats durchsucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="bf6de-111">An array to be searched using the given predicate.</span></span>



## <a name="output--int"></a><span data-ttu-id="bf6de-112">Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="bf6de-112">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="bf6de-113">Entweder der kleinste Index `idx` , der `predicate(arr[idx])` true ist, oder-1, wenn kein solches Element vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="bf6de-113">Either the smallest index `idx` such that `predicate(arr[idx])` is true, or -1 if no such element exists.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="bf6de-114">Typparameter</span><span class="sxs-lookup"><span data-stu-id="bf6de-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="bf6de-115">GIF</span><span class="sxs-lookup"><span data-stu-id="bf6de-115">'T</span></span>



## <a name="example"></a><span data-ttu-id="bf6de-116">Beispiel</span><span class="sxs-lookup"><span data-stu-id="bf6de-116">Example</span></span>

<span data-ttu-id="bf6de-117">Angenommen, `IsEven : Int -> Bool` Es handelt sich um eine Funktion, die nur dann zurückgibt, wenn `true` Ihre Eingabe gerade ist.</span><span class="sxs-lookup"><span data-stu-id="bf6de-117">Suppose that `IsEven : Int -> Bool` is a function that returns `true` if and only if its input is even.</span></span> <span data-ttu-id="bf6de-118">Anschließend kann dies mit verwendet werden, `IndexOf` um das erste gerade Element in einem Array zu finden:</span><span class="sxs-lookup"><span data-stu-id="bf6de-118">Then, this can be used with `IndexOf` to find the first even element in an array:</span></span>

```qsharp
let items = [1, 3, 17, 2, 21];
let idx = IndexOf(IsEven, items); // returns 3
```