---
uid: Microsoft.Quantum.Canon.Delayed
title: Verzögerte Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Delayed
qsharp.summary: Returns an operation that applies given operation with given argument.
ms.openlocfilehash: 863c63d0c1a50339e9d5b9fbe4729932b2706f32
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96216454"
---
# <a name="delayed-function"></a><span data-ttu-id="358eb-102">Verzögerte Funktion</span><span class="sxs-lookup"><span data-stu-id="358eb-102">Delayed function</span></span>

<span data-ttu-id="358eb-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="358eb-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="358eb-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="358eb-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="358eb-105">Gibt einen Vorgang zurück, der den angegebenen Vorgang mit dem angegebenen Argument anwendet.</span><span class="sxs-lookup"><span data-stu-id="358eb-105">Returns an operation that applies given operation with given argument.</span></span>

```qsharp
function Delayed<'T, 'U> (op : ('T => 'U), arg : 'T) : (Unit => 'U)
```


## <a name="input"></a><span data-ttu-id="358eb-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="358eb-106">Input</span></span>

### <a name="op--t--u"></a><span data-ttu-id="358eb-107">OP: 't => ' U</span><span class="sxs-lookup"><span data-stu-id="358eb-107">op : 'T => 'U</span></span> 

<span data-ttu-id="358eb-108">Ein anzuwendende Vorgang.</span><span class="sxs-lookup"><span data-stu-id="358eb-108">An operation to be applied.</span></span>


### <a name="arg--t"></a><span data-ttu-id="358eb-109">arg: 't</span><span class="sxs-lookup"><span data-stu-id="358eb-109">arg : 'T</span></span>

<span data-ttu-id="358eb-110">Die Eingabe, auf die der Vorgang angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="358eb-110">The input to which the operation is applied.</span></span>



## <a name="output--unit--u"></a><span data-ttu-id="358eb-111">Ausgabe: [Unit](xref:microsoft.quantum.lang-ref.unit) => ' U</span><span class="sxs-lookup"><span data-stu-id="358eb-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit) => 'U</span></span> 

<span data-ttu-id="358eb-112">Ein neuer Vorgang, der `op` mit Input angewendet wird. `arg`</span><span class="sxs-lookup"><span data-stu-id="358eb-112">A new operation which applies `op` with input `arg`</span></span>

## <a name="type-parameters"></a><span data-ttu-id="358eb-113">Typparameter</span><span class="sxs-lookup"><span data-stu-id="358eb-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="358eb-114">GIF</span><span class="sxs-lookup"><span data-stu-id="358eb-114">'T</span></span>

<span data-ttu-id="358eb-115">Der Eingabetyp des Vorgangs, der verzögert werden soll.</span><span class="sxs-lookup"><span data-stu-id="358eb-115">The input type of the operation to be delayed.</span></span>
### <a name="u"></a><span data-ttu-id="358eb-116">"U</span><span class="sxs-lookup"><span data-stu-id="358eb-116">'U</span></span>

<span data-ttu-id="358eb-117">Der Rückgabetyp des Vorgangs, der verzögert werden soll.</span><span class="sxs-lookup"><span data-stu-id="358eb-117">The return type of the operation to be delayed.</span></span>

## <a name="see-also"></a><span data-ttu-id="358eb-118">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="358eb-118">See Also</span></span>

- [<span data-ttu-id="358eb-119">Microsoft. Quantum. Canon. delayedc</span><span class="sxs-lookup"><span data-stu-id="358eb-119">Microsoft.Quantum.Canon.DelayedC</span></span>](xref:Microsoft.Quantum.Canon.DelayedC)
- [<span data-ttu-id="358eb-120">Microsoft. Quantum. Canon. delayeda</span><span class="sxs-lookup"><span data-stu-id="358eb-120">Microsoft.Quantum.Canon.DelayedA</span></span>](xref:Microsoft.Quantum.Canon.DelayedA)
- [<span data-ttu-id="358eb-121">Microsoft. Quantum. Canon. delayedca</span><span class="sxs-lookup"><span data-stu-id="358eb-121">Microsoft.Quantum.Canon.DelayedCA</span></span>](xref:Microsoft.Quantum.Canon.DelayedCA)
- [<span data-ttu-id="358eb-122">Microsoft. Quantum. Canon. Delay</span><span class="sxs-lookup"><span data-stu-id="358eb-122">Microsoft.Quantum.Canon.Delay</span></span>](xref:Microsoft.Quantum.Canon.Delay)