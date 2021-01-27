---
uid: Microsoft.Quantum.Canon.Delayed
title: Verzögerte Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Delayed
qsharp.summary: Returns an operation that applies given operation with given argument.
ms.openlocfilehash: 40fcc7d0a178fdb18437b4d6c96542db593347b4
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840585"
---
# <a name="delayed-function"></a><span data-ttu-id="f21e2-102">Verzögerte Funktion</span><span class="sxs-lookup"><span data-stu-id="f21e2-102">Delayed function</span></span>

<span data-ttu-id="f21e2-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="f21e2-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="f21e2-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="f21e2-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="f21e2-105">Gibt einen Vorgang zurück, der den angegebenen Vorgang mit dem angegebenen Argument anwendet.</span><span class="sxs-lookup"><span data-stu-id="f21e2-105">Returns an operation that applies given operation with given argument.</span></span>

```qsharp
function Delayed<'T, 'U> (op : ('T => 'U), arg : 'T) : (Unit => 'U)
```


## <a name="input"></a><span data-ttu-id="f21e2-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f21e2-106">Input</span></span>

### <a name="op--t--u"></a><span data-ttu-id="f21e2-107">OP: 't => ' U</span><span class="sxs-lookup"><span data-stu-id="f21e2-107">op : 'T => 'U</span></span> 

<span data-ttu-id="f21e2-108">Ein anzuwendende Vorgang.</span><span class="sxs-lookup"><span data-stu-id="f21e2-108">An operation to be applied.</span></span>


### <a name="arg--t"></a><span data-ttu-id="f21e2-109">arg: 't</span><span class="sxs-lookup"><span data-stu-id="f21e2-109">arg : 'T</span></span>

<span data-ttu-id="f21e2-110">Die Eingabe, auf die der Vorgang angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="f21e2-110">The input to which the operation is applied.</span></span>



## <a name="output--unit--u"></a><span data-ttu-id="f21e2-111">Ausgabe: [Unit](xref:microsoft.quantum.lang-ref.unit) => ' U</span><span class="sxs-lookup"><span data-stu-id="f21e2-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit) => 'U</span></span> 

<span data-ttu-id="f21e2-112">Ein neuer Vorgang, der `op` mit Input angewendet wird. `arg`</span><span class="sxs-lookup"><span data-stu-id="f21e2-112">A new operation which applies `op` with input `arg`</span></span>

## <a name="type-parameters"></a><span data-ttu-id="f21e2-113">Typparameter</span><span class="sxs-lookup"><span data-stu-id="f21e2-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="f21e2-114">GIF</span><span class="sxs-lookup"><span data-stu-id="f21e2-114">'T</span></span>

<span data-ttu-id="f21e2-115">Der Eingabetyp des Vorgangs, der verzögert werden soll.</span><span class="sxs-lookup"><span data-stu-id="f21e2-115">The input type of the operation to be delayed.</span></span>
### <a name="u"></a><span data-ttu-id="f21e2-116">"U</span><span class="sxs-lookup"><span data-stu-id="f21e2-116">'U</span></span>

<span data-ttu-id="f21e2-117">Der Rückgabetyp des Vorgangs, der verzögert werden soll.</span><span class="sxs-lookup"><span data-stu-id="f21e2-117">The return type of the operation to be delayed.</span></span>

## <a name="see-also"></a><span data-ttu-id="f21e2-118">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="f21e2-118">See Also</span></span>

- [<span data-ttu-id="f21e2-119">Microsoft. Quantum. Canon. delayedc</span><span class="sxs-lookup"><span data-stu-id="f21e2-119">Microsoft.Quantum.Canon.DelayedC</span></span>](xref:Microsoft.Quantum.Canon.DelayedC)
- [<span data-ttu-id="f21e2-120">Microsoft. Quantum. Canon. delayeda</span><span class="sxs-lookup"><span data-stu-id="f21e2-120">Microsoft.Quantum.Canon.DelayedA</span></span>](xref:Microsoft.Quantum.Canon.DelayedA)
- [<span data-ttu-id="f21e2-121">Microsoft. Quantum. Canon. delayedca</span><span class="sxs-lookup"><span data-stu-id="f21e2-121">Microsoft.Quantum.Canon.DelayedCA</span></span>](xref:Microsoft.Quantum.Canon.DelayedCA)
- [<span data-ttu-id="f21e2-122">Microsoft. Quantum. Canon. Delay</span><span class="sxs-lookup"><span data-stu-id="f21e2-122">Microsoft.Quantum.Canon.Delay</span></span>](xref:Microsoft.Quantum.Canon.Delay)