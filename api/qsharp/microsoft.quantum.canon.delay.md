---
uid: Microsoft.Quantum.Canon.Delay
title: Verzögerungs Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Delay
qsharp.summary: Applies a given operation with a delay.
ms.openlocfilehash: c8ba128e44a9b217ec196e39ff1df639ef276784
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840654"
---
# <a name="delay-operation"></a><span data-ttu-id="a3135-102">Verzögerungs Vorgang</span><span class="sxs-lookup"><span data-stu-id="a3135-102">Delay operation</span></span>

<span data-ttu-id="a3135-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="a3135-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="a3135-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a3135-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="a3135-105">Wendet einen angegebenen Vorgang mit einer Verzögerung an.</span><span class="sxs-lookup"><span data-stu-id="a3135-105">Applies a given operation with a delay.</span></span>

```qsharp
operation Delay<'T, 'U> (op : ('T => 'U), arg : 'T, aux : Unit) : 'U
```


## <a name="description"></a><span data-ttu-id="a3135-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a3135-106">Description</span></span>

<span data-ttu-id="a3135-107">Wenn ein Vorgang und eine Eingabe für diesen Vorgang vorhanden sind, wendet den Vorgang an, sobald eine zusätzliche Eingabe bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="a3135-107">Given an operation and an input to that operation, applies the operation once an additional input is provided.</span></span>
<span data-ttu-id="a3135-108">Der-Ausdruck ist insbesondere `Delay(op, arg, _)` ein Vorgang, der `op` sich auf bezieht, `arg` Wenn aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="a3135-108">In particular, the expression `Delay(op, arg, _)` is an operation that applies `op` to `arg` when called.</span></span>
<span data-ttu-id="a3135-109">`Delay(op,arg,_)`Der Ausdruck ermöglicht das Verzögern der Anwendung von `op` .</span><span class="sxs-lookup"><span data-stu-id="a3135-109">Expression `Delay(op,arg,_)` allows to delay the application of `op`.</span></span>

## <a name="input"></a><span data-ttu-id="a3135-110">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a3135-110">Input</span></span>

### <a name="op--t--u"></a><span data-ttu-id="a3135-111">OP: 't => ' U</span><span class="sxs-lookup"><span data-stu-id="a3135-111">op : 'T => 'U</span></span> 

<span data-ttu-id="a3135-112">Ein anzuwendende Vorgang.</span><span class="sxs-lookup"><span data-stu-id="a3135-112">An operation to be applied.</span></span>


### <a name="arg--t"></a><span data-ttu-id="a3135-113">arg: 't</span><span class="sxs-lookup"><span data-stu-id="a3135-113">arg : 'T</span></span>

<span data-ttu-id="a3135-114">Die Eingabe, auf die der Vorgang angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="a3135-114">The input to which the operation is applied.</span></span>


### <a name="aux--unit"></a><span data-ttu-id="a3135-115">AUX: [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="a3135-115">aux : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

<span data-ttu-id="a3135-116">Argument, das verwendet wird, um die Anwendung des Vorgangs mithilfe der partiellen Anwendung zu verzögern.</span><span class="sxs-lookup"><span data-stu-id="a3135-116">Argument used to delay the application of operation by using partial application.</span></span>



## <a name="output--u"></a><span data-ttu-id="a3135-117">Ausgabe: "U</span><span class="sxs-lookup"><span data-stu-id="a3135-117">Output : 'U</span></span>



## <a name="type-parameters"></a><span data-ttu-id="a3135-118">Typparameter</span><span class="sxs-lookup"><span data-stu-id="a3135-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="a3135-119">GIF</span><span class="sxs-lookup"><span data-stu-id="a3135-119">'T</span></span>

<span data-ttu-id="a3135-120">Der Eingabetyp des Vorgangs, der verzögert werden soll.</span><span class="sxs-lookup"><span data-stu-id="a3135-120">The input type of the operation to be delayed.</span></span>
### <a name="u"></a><span data-ttu-id="a3135-121">"U</span><span class="sxs-lookup"><span data-stu-id="a3135-121">'U</span></span>

<span data-ttu-id="a3135-122">Der Rückgabetyp des Vorgangs, der verzögert werden soll.</span><span class="sxs-lookup"><span data-stu-id="a3135-122">The return type of the operation to be delayed.</span></span>

## <a name="see-also"></a><span data-ttu-id="a3135-123">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="a3135-123">See Also</span></span>

- [<span data-ttu-id="a3135-124">Microsoft. Quantum. Canon. Delta-c</span><span class="sxs-lookup"><span data-stu-id="a3135-124">Microsoft.Quantum.Canon.DelayC</span></span>](xref:Microsoft.Quantum.Canon.DelayC)
- [<span data-ttu-id="a3135-125">Microsoft. Quantum. Canon. Delaya</span><span class="sxs-lookup"><span data-stu-id="a3135-125">Microsoft.Quantum.Canon.DelayA</span></span>](xref:Microsoft.Quantum.Canon.DelayA)
- [<span data-ttu-id="a3135-126">Microsoft. Quantum. Canon. Delta-ca</span><span class="sxs-lookup"><span data-stu-id="a3135-126">Microsoft.Quantum.Canon.DelayCA</span></span>](xref:Microsoft.Quantum.Canon.DelayCA)
- [<span data-ttu-id="a3135-127">Microsoft. Quantum. Canon. verzögert</span><span class="sxs-lookup"><span data-stu-id="a3135-127">Microsoft.Quantum.Canon.Delayed</span></span>](xref:Microsoft.Quantum.Canon.Delayed)