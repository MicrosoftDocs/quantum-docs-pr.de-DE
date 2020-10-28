---
uid: Microsoft.Quantum.Canon.DelayedA
title: Delayeda-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: DelayedA
qsharp.summary: Returns an operation that applies given operation with given argument.
ms.openlocfilehash: 11c11cdd75d80d6324666ef56930f7a522121826
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704215"
---
# <a name="delayeda-function"></a><span data-ttu-id="a6cf6-102">Delayeda-Funktion</span><span class="sxs-lookup"><span data-stu-id="a6cf6-102">DelayedA function</span></span>

<span data-ttu-id="a6cf6-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="a6cf6-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="a6cf6-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="a6cf6-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="a6cf6-105">Gibt einen Vorgang zurück, der den angegebenen Vorgang mit dem angegebenen Argument anwendet.</span><span class="sxs-lookup"><span data-stu-id="a6cf6-105">Returns an operation that applies given operation with given argument.</span></span>

```qsharp
function DelayedA<'T> (op : ('T => Unit is Adj), arg : 'T) : (Unit => Unit is Adj)
```


## <a name="input"></a><span data-ttu-id="a6cf6-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a6cf6-106">Input</span></span>

### <a name="op--t--unit-adj"></a><span data-ttu-id="a6cf6-107">OP: 't => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ</span><span class="sxs-lookup"><span data-stu-id="a6cf6-107">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="a6cf6-108">Ein Vorgang, der als Ergebnis der Anwendung eines Rückgabewerts angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a6cf6-108">An operation to be applied as a result of applying return value</span></span>


### <a name="arg--t"></a><span data-ttu-id="a6cf6-109">arg: 't</span><span class="sxs-lookup"><span data-stu-id="a6cf6-109">arg : 'T</span></span>

<span data-ttu-id="a6cf6-110">Die Eingabe, auf die der Vorgang `op` angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="a6cf6-110">The input to which the operation `op` is applied.</span></span>



## <a name="output--unit--unit-adj"></a><span data-ttu-id="a6cf6-111">Ausgabe: [Unit](xref:microsoft.quantum.lang-ref.unit) => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ</span><span class="sxs-lookup"><span data-stu-id="a6cf6-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit) => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="a6cf6-112">Ein neuer Vorgang, der `op` mit Input angewendet wird. `arg`</span><span class="sxs-lookup"><span data-stu-id="a6cf6-112">A new operation which applies `op` with input `arg`</span></span>

## <a name="type-parameters"></a><span data-ttu-id="a6cf6-113">Typparameter</span><span class="sxs-lookup"><span data-stu-id="a6cf6-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="a6cf6-114">GIF</span><span class="sxs-lookup"><span data-stu-id="a6cf6-114">'T</span></span>

<span data-ttu-id="a6cf6-115">Der Eingabetyp des Vorgangs, der verzögert werden soll.</span><span class="sxs-lookup"><span data-stu-id="a6cf6-115">The input type of the operation to be delayed.</span></span>

## <a name="see-also"></a><span data-ttu-id="a6cf6-116">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="a6cf6-116">See Also</span></span>

- [<span data-ttu-id="a6cf6-117">Microsoft. Quantum. Canon. verzögert</span><span class="sxs-lookup"><span data-stu-id="a6cf6-117">Microsoft.Quantum.Canon.Delayed</span></span>](xref:Microsoft.Quantum.Canon.Delayed)
- [<span data-ttu-id="a6cf6-118">Microsoft. Quantum. Canon. Delay</span><span class="sxs-lookup"><span data-stu-id="a6cf6-118">Microsoft.Quantum.Canon.Delay</span></span>](xref:Microsoft.Quantum.Canon.Delay)