---
uid: Microsoft.Quantum.Canon.DelayedA
title: Delayeda-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: DelayedA
qsharp.summary: Returns an operation that applies given operation with given argument.
ms.openlocfilehash: e53279bd3ddc5fa8bc0c862f998b273a9e17a85b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840599"
---
# <a name="delayeda-function"></a><span data-ttu-id="e9795-102">Delayeda-Funktion</span><span class="sxs-lookup"><span data-stu-id="e9795-102">DelayedA function</span></span>

<span data-ttu-id="e9795-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="e9795-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="e9795-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="e9795-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="e9795-105">Gibt einen Vorgang zurück, der den angegebenen Vorgang mit dem angegebenen Argument anwendet.</span><span class="sxs-lookup"><span data-stu-id="e9795-105">Returns an operation that applies given operation with given argument.</span></span>

```qsharp
function DelayedA<'T> (op : ('T => Unit is Adj), arg : 'T) : (Unit => Unit is Adj)
```


## <a name="input"></a><span data-ttu-id="e9795-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e9795-106">Input</span></span>

### <a name="op--t--unit--is-adj"></a><span data-ttu-id="e9795-107">OP: 't => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ</span><span class="sxs-lookup"><span data-stu-id="e9795-107">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="e9795-108">Ein Vorgang, der als Ergebnis der Anwendung eines Rückgabewerts angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="e9795-108">An operation to be applied as a result of applying return value</span></span>


### <a name="arg--t"></a><span data-ttu-id="e9795-109">arg: 't</span><span class="sxs-lookup"><span data-stu-id="e9795-109">arg : 'T</span></span>

<span data-ttu-id="e9795-110">Die Eingabe, auf die der Vorgang `op` angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="e9795-110">The input to which the operation `op` is applied.</span></span>



## <a name="output--unit--unit--is-adj"></a><span data-ttu-id="e9795-111">Ausgabe: [Einheiten](xref:microsoft.quantum.lang-ref.unit) => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ</span><span class="sxs-lookup"><span data-stu-id="e9795-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="e9795-112">Ein neuer Vorgang, der `op` mit Input angewendet wird. `arg`</span><span class="sxs-lookup"><span data-stu-id="e9795-112">A new operation which applies `op` with input `arg`</span></span>

## <a name="type-parameters"></a><span data-ttu-id="e9795-113">Typparameter</span><span class="sxs-lookup"><span data-stu-id="e9795-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="e9795-114">GIF</span><span class="sxs-lookup"><span data-stu-id="e9795-114">'T</span></span>

<span data-ttu-id="e9795-115">Der Eingabetyp des Vorgangs, der verzögert werden soll.</span><span class="sxs-lookup"><span data-stu-id="e9795-115">The input type of the operation to be delayed.</span></span>

## <a name="see-also"></a><span data-ttu-id="e9795-116">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e9795-116">See Also</span></span>

- [<span data-ttu-id="e9795-117">Microsoft. Quantum. Canon. verzögert</span><span class="sxs-lookup"><span data-stu-id="e9795-117">Microsoft.Quantum.Canon.Delayed</span></span>](xref:Microsoft.Quantum.Canon.Delayed)
- [<span data-ttu-id="e9795-118">Microsoft. Quantum. Canon. Delay</span><span class="sxs-lookup"><span data-stu-id="e9795-118">Microsoft.Quantum.Canon.Delay</span></span>](xref:Microsoft.Quantum.Canon.Delay)