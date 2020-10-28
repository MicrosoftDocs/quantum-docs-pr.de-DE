---
uid: Microsoft.Quantum.Canon.DelayCA
title: Delta-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: DelayCA
qsharp.summary: Applies a given operation with a delay.
ms.openlocfilehash: 4b4be55436d6619511a12c6fb7fbd0f23989152a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704226"
---
# <a name="delayca-operation"></a><span data-ttu-id="f901b-102">Delta-Vorgang</span><span class="sxs-lookup"><span data-stu-id="f901b-102">DelayCA operation</span></span>

<span data-ttu-id="f901b-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="f901b-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="f901b-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="f901b-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="f901b-105">Wendet einen angegebenen Vorgang mit einer Verzögerung an.</span><span class="sxs-lookup"><span data-stu-id="f901b-105">Applies a given operation with a delay.</span></span>

```qsharp
operation DelayCA<'T> (op : ('T => Unit is Ctl + Adj), arg : 'T, aux : Unit) : Unit
```


## <a name="description"></a><span data-ttu-id="f901b-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f901b-106">Description</span></span>

<span data-ttu-id="f901b-107">Wenn ein Vorgang und eine Eingabe für diesen Vorgang vorhanden sind, wendet den Vorgang an, sobald eine zusätzliche Eingabe bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="f901b-107">Given an operation and an input to that operation, applies the operation once an additional input is provided.</span></span>
<span data-ttu-id="f901b-108">Der-Ausdruck ist insbesondere `Delay(op, arg, _)` ein Vorgang, der `op` sich auf bezieht, `arg` Wenn aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="f901b-108">In particular, the expression `Delay(op, arg, _)` is an operation that applies `op` to `arg` when called.</span></span>
<span data-ttu-id="f901b-109">`Delay(op,arg,_)`Der Ausdruck ermöglicht das Verzögern der Anwendung von `op` .</span><span class="sxs-lookup"><span data-stu-id="f901b-109">Expression `Delay(op,arg,_)` allows to delay the application of `op`.</span></span>

## <a name="input"></a><span data-ttu-id="f901b-110">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f901b-110">Input</span></span>

### <a name="op--t--unit-ctl--adj"></a><span data-ttu-id="f901b-111">OP: 't => [Unit](xref:microsoft.quantum.lang-ref.unit) CTL + ADJ</span><span class="sxs-lookup"><span data-stu-id="f901b-111">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl + Adj</span></span>

<span data-ttu-id="f901b-112">Ein anzuwendende Vorgang.</span><span class="sxs-lookup"><span data-stu-id="f901b-112">An operation to be applied.</span></span>


### <a name="arg--t"></a><span data-ttu-id="f901b-113">arg: 't</span><span class="sxs-lookup"><span data-stu-id="f901b-113">arg : 'T</span></span>

<span data-ttu-id="f901b-114">Die Eingabe, auf die der Vorgang angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="f901b-114">The input to which the operation is applied.</span></span>


### <a name="aux--unit"></a><span data-ttu-id="f901b-115">AUX: [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="f901b-115">aux : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

<span data-ttu-id="f901b-116">Argument, das verwendet wird, um die Anwendung des Vorgangs mithilfe der partiellen Anwendung zu verzögern.</span><span class="sxs-lookup"><span data-stu-id="f901b-116">Argument used to delay the application of operation by using partial application.</span></span>



## <a name="output--unit"></a><span data-ttu-id="f901b-117">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="f901b-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="f901b-118">Typparameter</span><span class="sxs-lookup"><span data-stu-id="f901b-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="f901b-119">GIF</span><span class="sxs-lookup"><span data-stu-id="f901b-119">'T</span></span>

<span data-ttu-id="f901b-120">Der Eingabetyp des Vorgangs, der verzögert werden soll.</span><span class="sxs-lookup"><span data-stu-id="f901b-120">The input type of the operation to be delayed.</span></span>

## <a name="see-also"></a><span data-ttu-id="f901b-121">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="f901b-121">See Also</span></span>

- [<span data-ttu-id="f901b-122">Microsoft. Quantum. Canon. Delay</span><span class="sxs-lookup"><span data-stu-id="f901b-122">Microsoft.Quantum.Canon.Delay</span></span>](xref:Microsoft.Quantum.Canon.Delay)
- [<span data-ttu-id="f901b-123">Microsoft. Quantum. Canon. verzögert</span><span class="sxs-lookup"><span data-stu-id="f901b-123">Microsoft.Quantum.Canon.Delayed</span></span>](xref:Microsoft.Quantum.Canon.Delayed)