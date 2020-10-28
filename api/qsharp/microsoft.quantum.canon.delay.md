---
uid: Microsoft.Quantum.Canon.Delay
title: Verzögerungs Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Delay
qsharp.summary: Applies a given operation with a delay.
ms.openlocfilehash: f9f0e5c3120eb69bd7431d52d6cde5e846ffbe4d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704255"
---
# <a name="delay-operation"></a><span data-ttu-id="6d99f-102">Verzögerungs Vorgang</span><span class="sxs-lookup"><span data-stu-id="6d99f-102">Delay operation</span></span>

<span data-ttu-id="6d99f-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="6d99f-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="6d99f-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="6d99f-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="6d99f-105">Wendet einen angegebenen Vorgang mit einer Verzögerung an.</span><span class="sxs-lookup"><span data-stu-id="6d99f-105">Applies a given operation with a delay.</span></span>

```qsharp
operation Delay<'T, 'U> (op : ('T => 'U), arg : 'T, aux : Unit) : 'U
```


## <a name="description"></a><span data-ttu-id="6d99f-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6d99f-106">Description</span></span>

<span data-ttu-id="6d99f-107">Wenn ein Vorgang und eine Eingabe für diesen Vorgang vorhanden sind, wendet den Vorgang an, sobald eine zusätzliche Eingabe bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="6d99f-107">Given an operation and an input to that operation, applies the operation once an additional input is provided.</span></span>
<span data-ttu-id="6d99f-108">Der-Ausdruck ist insbesondere `Delay(op, arg, _)` ein Vorgang, der `op` sich auf bezieht, `arg` Wenn aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="6d99f-108">In particular, the expression `Delay(op, arg, _)` is an operation that applies `op` to `arg` when called.</span></span>
<span data-ttu-id="6d99f-109">`Delay(op,arg,_)`Der Ausdruck ermöglicht das Verzögern der Anwendung von `op` .</span><span class="sxs-lookup"><span data-stu-id="6d99f-109">Expression `Delay(op,arg,_)` allows to delay the application of `op`.</span></span>

## <a name="input"></a><span data-ttu-id="6d99f-110">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6d99f-110">Input</span></span>

### <a name="op--t--u"></a><span data-ttu-id="6d99f-111">OP: 't => ' U</span><span class="sxs-lookup"><span data-stu-id="6d99f-111">op : 'T => 'U</span></span> 

<span data-ttu-id="6d99f-112">Ein anzuwendende Vorgang.</span><span class="sxs-lookup"><span data-stu-id="6d99f-112">An operation to be applied.</span></span>


### <a name="arg--t"></a><span data-ttu-id="6d99f-113">arg: 't</span><span class="sxs-lookup"><span data-stu-id="6d99f-113">arg : 'T</span></span>

<span data-ttu-id="6d99f-114">Die Eingabe, auf die der Vorgang angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="6d99f-114">The input to which the operation is applied.</span></span>


### <a name="aux--unit"></a><span data-ttu-id="6d99f-115">AUX: [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="6d99f-115">aux : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

<span data-ttu-id="6d99f-116">Argument, das verwendet wird, um die Anwendung des Vorgangs mithilfe der partiellen Anwendung zu verzögern.</span><span class="sxs-lookup"><span data-stu-id="6d99f-116">Argument used to delay the application of operation by using partial application.</span></span>



## <a name="output--u"></a><span data-ttu-id="6d99f-117">Ausgabe: "U</span><span class="sxs-lookup"><span data-stu-id="6d99f-117">Output : 'U</span></span>



## <a name="type-parameters"></a><span data-ttu-id="6d99f-118">Typparameter</span><span class="sxs-lookup"><span data-stu-id="6d99f-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="6d99f-119">GIF</span><span class="sxs-lookup"><span data-stu-id="6d99f-119">'T</span></span>

<span data-ttu-id="6d99f-120">Der Eingabetyp des Vorgangs, der verzögert werden soll.</span><span class="sxs-lookup"><span data-stu-id="6d99f-120">The input type of the operation to be delayed.</span></span>
### <a name="u"></a><span data-ttu-id="6d99f-121">"U</span><span class="sxs-lookup"><span data-stu-id="6d99f-121">'U</span></span>

<span data-ttu-id="6d99f-122">Der Rückgabetyp des Vorgangs, der verzögert werden soll.</span><span class="sxs-lookup"><span data-stu-id="6d99f-122">The return type of the operation to be delayed.</span></span>

## <a name="see-also"></a><span data-ttu-id="6d99f-123">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="6d99f-123">See Also</span></span>

- [<span data-ttu-id="6d99f-124">Microsoft. Quantum. Canon. Delta-c</span><span class="sxs-lookup"><span data-stu-id="6d99f-124">Microsoft.Quantum.Canon.DelayC</span></span>](xref:Microsoft.Quantum.Canon.DelayC)
- [<span data-ttu-id="6d99f-125">Microsoft. Quantum. Canon. Delaya</span><span class="sxs-lookup"><span data-stu-id="6d99f-125">Microsoft.Quantum.Canon.DelayA</span></span>](xref:Microsoft.Quantum.Canon.DelayA)
- [<span data-ttu-id="6d99f-126">Microsoft. Quantum. Canon. Delta-ca</span><span class="sxs-lookup"><span data-stu-id="6d99f-126">Microsoft.Quantum.Canon.DelayCA</span></span>](xref:Microsoft.Quantum.Canon.DelayCA)
- [<span data-ttu-id="6d99f-127">Microsoft. Quantum. Canon. verzögert</span><span class="sxs-lookup"><span data-stu-id="6d99f-127">Microsoft.Quantum.Canon.Delayed</span></span>](xref:Microsoft.Quantum.Canon.Delayed)