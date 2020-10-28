---
uid: Microsoft.Quantum.Canon.Delayed
title: Verzögerte Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Delayed
qsharp.summary: Returns an operation that applies given operation with given argument.
ms.openlocfilehash: 820a38c2b4de2e0151d55bd88fb4f69567182f6b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704218"
---
# <a name="delayed-function"></a><span data-ttu-id="6808b-102">Verzögerte Funktion</span><span class="sxs-lookup"><span data-stu-id="6808b-102">Delayed function</span></span>

<span data-ttu-id="6808b-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="6808b-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="6808b-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="6808b-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="6808b-105">Gibt einen Vorgang zurück, der den angegebenen Vorgang mit dem angegebenen Argument anwendet.</span><span class="sxs-lookup"><span data-stu-id="6808b-105">Returns an operation that applies given operation with given argument.</span></span>

```qsharp
function Delayed<'T, 'U> (op : ('T => 'U), arg : 'T) : (Unit => 'U)
```


## <a name="input"></a><span data-ttu-id="6808b-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6808b-106">Input</span></span>

### <a name="op--t--u"></a><span data-ttu-id="6808b-107">OP: 't => ' U</span><span class="sxs-lookup"><span data-stu-id="6808b-107">op : 'T => 'U</span></span> 

<span data-ttu-id="6808b-108">Ein anzuwendende Vorgang.</span><span class="sxs-lookup"><span data-stu-id="6808b-108">An operation to be applied.</span></span>


### <a name="arg--t"></a><span data-ttu-id="6808b-109">arg: 't</span><span class="sxs-lookup"><span data-stu-id="6808b-109">arg : 'T</span></span>

<span data-ttu-id="6808b-110">Die Eingabe, auf die der Vorgang angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="6808b-110">The input to which the operation is applied.</span></span>



## <a name="output--unit--u"></a><span data-ttu-id="6808b-111">Ausgabe: [Unit](xref:microsoft.quantum.lang-ref.unit) => ' U</span><span class="sxs-lookup"><span data-stu-id="6808b-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit) => 'U</span></span> 

<span data-ttu-id="6808b-112">Ein neuer Vorgang, der `op` mit Input angewendet wird. `arg`</span><span class="sxs-lookup"><span data-stu-id="6808b-112">A new operation which applies `op` with input `arg`</span></span>

## <a name="type-parameters"></a><span data-ttu-id="6808b-113">Typparameter</span><span class="sxs-lookup"><span data-stu-id="6808b-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="6808b-114">GIF</span><span class="sxs-lookup"><span data-stu-id="6808b-114">'T</span></span>

<span data-ttu-id="6808b-115">Der Eingabetyp des Vorgangs, der verzögert werden soll.</span><span class="sxs-lookup"><span data-stu-id="6808b-115">The input type of the operation to be delayed.</span></span>
### <a name="u"></a><span data-ttu-id="6808b-116">"U</span><span class="sxs-lookup"><span data-stu-id="6808b-116">'U</span></span>

<span data-ttu-id="6808b-117">Der Rückgabetyp des Vorgangs, der verzögert werden soll.</span><span class="sxs-lookup"><span data-stu-id="6808b-117">The return type of the operation to be delayed.</span></span>

## <a name="see-also"></a><span data-ttu-id="6808b-118">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="6808b-118">See Also</span></span>

- [<span data-ttu-id="6808b-119">Microsoft. Quantum. Canon. delayedc</span><span class="sxs-lookup"><span data-stu-id="6808b-119">Microsoft.Quantum.Canon.DelayedC</span></span>](xref:Microsoft.Quantum.Canon.DelayedC)
- [<span data-ttu-id="6808b-120">Microsoft. Quantum. Canon. delayeda</span><span class="sxs-lookup"><span data-stu-id="6808b-120">Microsoft.Quantum.Canon.DelayedA</span></span>](xref:Microsoft.Quantum.Canon.DelayedA)
- [<span data-ttu-id="6808b-121">Microsoft. Quantum. Canon. delayedca</span><span class="sxs-lookup"><span data-stu-id="6808b-121">Microsoft.Quantum.Canon.DelayedCA</span></span>](xref:Microsoft.Quantum.Canon.DelayedCA)
- [<span data-ttu-id="6808b-122">Microsoft. Quantum. Canon. Delay</span><span class="sxs-lookup"><span data-stu-id="6808b-122">Microsoft.Quantum.Canon.Delay</span></span>](xref:Microsoft.Quantum.Canon.Delay)