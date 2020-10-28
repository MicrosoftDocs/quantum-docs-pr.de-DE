---
uid: Microsoft.Quantum.Canon.DelayedCA
title: Delayedca-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: DelayedCA
qsharp.summary: Returns an operation that applies given operation with given argument.
ms.openlocfilehash: 8ee55e2ca7ec2cff9618b5dc66e19d88779d39ce
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704199"
---
# <a name="delayedca-function"></a><span data-ttu-id="8293f-102">Delayedca-Funktion</span><span class="sxs-lookup"><span data-stu-id="8293f-102">DelayedCA function</span></span>

<span data-ttu-id="8293f-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="8293f-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="8293f-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="8293f-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="8293f-105">Gibt einen Vorgang zurück, der den angegebenen Vorgang mit dem angegebenen Argument anwendet.</span><span class="sxs-lookup"><span data-stu-id="8293f-105">Returns an operation that applies given operation with given argument.</span></span>

```qsharp
function DelayedCA<'T> (op : ('T => Unit is Ctl + Adj), arg : 'T) : (Unit => Unit is Ctl + Adj)
```


## <a name="input"></a><span data-ttu-id="8293f-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8293f-106">Input</span></span>

### <a name="op--t--unit-ctl--adj"></a><span data-ttu-id="8293f-107">OP: 't => [Unit](xref:microsoft.quantum.lang-ref.unit) CTL + ADJ</span><span class="sxs-lookup"><span data-stu-id="8293f-107">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl + Adj</span></span>

<span data-ttu-id="8293f-108">Ein Vorgang, der als Ergebnis der Anwendung eines Rückgabewerts angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="8293f-108">An operation to be applied as a result of applying return value</span></span>


### <a name="arg--t"></a><span data-ttu-id="8293f-109">arg: 't</span><span class="sxs-lookup"><span data-stu-id="8293f-109">arg : 'T</span></span>

<span data-ttu-id="8293f-110">Die Eingabe, auf die der Vorgang `op` angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="8293f-110">The input to which the operation `op` is applied.</span></span>



## <a name="output--unit--unit-ctl--adj"></a><span data-ttu-id="8293f-111">Ausgabe: [Unit](xref:microsoft.quantum.lang-ref.unit) => [Unit](xref:microsoft.quantum.lang-ref.unit) CTL + ADJ</span><span class="sxs-lookup"><span data-stu-id="8293f-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit) => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl + Adj</span></span>

<span data-ttu-id="8293f-112">Ein neuer Vorgang, der `op` mit Input angewendet wird. `arg`</span><span class="sxs-lookup"><span data-stu-id="8293f-112">A new operation which applies `op` with input `arg`</span></span>

## <a name="type-parameters"></a><span data-ttu-id="8293f-113">Typparameter</span><span class="sxs-lookup"><span data-stu-id="8293f-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="8293f-114">GIF</span><span class="sxs-lookup"><span data-stu-id="8293f-114">'T</span></span>

<span data-ttu-id="8293f-115">Der Eingabetyp des Vorgangs, der verzögert werden soll.</span><span class="sxs-lookup"><span data-stu-id="8293f-115">The input type of the operation to be delayed.</span></span>

## <a name="see-also"></a><span data-ttu-id="8293f-116">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="8293f-116">See Also</span></span>

- [<span data-ttu-id="8293f-117">Microsoft. Quantum. Canon. verzögert</span><span class="sxs-lookup"><span data-stu-id="8293f-117">Microsoft.Quantum.Canon.Delayed</span></span>](xref:Microsoft.Quantum.Canon.Delayed)
- [<span data-ttu-id="8293f-118">Microsoft. Quantum. Canon. Delay</span><span class="sxs-lookup"><span data-stu-id="8293f-118">Microsoft.Quantum.Canon.Delay</span></span>](xref:Microsoft.Quantum.Canon.Delay)