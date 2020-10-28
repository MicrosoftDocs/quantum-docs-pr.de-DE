---
uid: Microsoft.Quantum.Canon.DelayC
title: Delta-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: DelayC
qsharp.summary: Applies a given operation with a delay.
ms.openlocfilehash: acb817c3322063353dc08c5d6f8c539391b3bf39
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704239"
---
# <a name="delayc-operation"></a><span data-ttu-id="ec1b1-102">Delta-Vorgang</span><span class="sxs-lookup"><span data-stu-id="ec1b1-102">DelayC operation</span></span>

<span data-ttu-id="ec1b1-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="ec1b1-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="ec1b1-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="ec1b1-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="ec1b1-105">Wendet einen angegebenen Vorgang mit einer Verzögerung an.</span><span class="sxs-lookup"><span data-stu-id="ec1b1-105">Applies a given operation with a delay.</span></span>

```qsharp
operation DelayC<'T> (op : ('T => Unit is Ctl), arg : 'T, aux : Unit) : Unit
```


## <a name="description"></a><span data-ttu-id="ec1b1-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ec1b1-106">Description</span></span>

<span data-ttu-id="ec1b1-107">Wenn ein Vorgang und eine Eingabe für diesen Vorgang vorhanden sind, wendet den Vorgang an, sobald eine zusätzliche Eingabe bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="ec1b1-107">Given an operation and an input to that operation, applies the operation once an additional input is provided.</span></span>
<span data-ttu-id="ec1b1-108">Der-Ausdruck ist insbesondere `Delay(op, arg, _)` ein Vorgang, der `op` sich auf bezieht, `arg` Wenn aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="ec1b1-108">In particular, the expression `Delay(op, arg, _)` is an operation that applies `op` to `arg` when called.</span></span>
<span data-ttu-id="ec1b1-109">`Delay(op,arg,_)`Der Ausdruck ermöglicht das Verzögern der Anwendung von `op` .</span><span class="sxs-lookup"><span data-stu-id="ec1b1-109">Expression `Delay(op,arg,_)` allows to delay the application of `op`.</span></span>

## <a name="input"></a><span data-ttu-id="ec1b1-110">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ec1b1-110">Input</span></span>

### <a name="op--t--unit-ctl"></a><span data-ttu-id="ec1b1-111">OP: 't => [Unit](xref:microsoft.quantum.lang-ref.unit) CTL</span><span class="sxs-lookup"><span data-stu-id="ec1b1-111">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>

<span data-ttu-id="ec1b1-112">Ein anzuwendende Vorgang.</span><span class="sxs-lookup"><span data-stu-id="ec1b1-112">An operation to be applied.</span></span>


### <a name="arg--t"></a><span data-ttu-id="ec1b1-113">arg: 't</span><span class="sxs-lookup"><span data-stu-id="ec1b1-113">arg : 'T</span></span>

<span data-ttu-id="ec1b1-114">Die Eingabe, auf die der Vorgang angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="ec1b1-114">The input to which the operation is applied.</span></span>


### <a name="aux--unit"></a><span data-ttu-id="ec1b1-115">AUX: [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="ec1b1-115">aux : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

<span data-ttu-id="ec1b1-116">Argument, das verwendet wird, um die Anwendung des Vorgangs mithilfe der partiellen Anwendung zu verzögern.</span><span class="sxs-lookup"><span data-stu-id="ec1b1-116">Argument used to delay the application of operation by using partial application.</span></span>



## <a name="output--unit"></a><span data-ttu-id="ec1b1-117">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="ec1b1-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="ec1b1-118">Typparameter</span><span class="sxs-lookup"><span data-stu-id="ec1b1-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="ec1b1-119">GIF</span><span class="sxs-lookup"><span data-stu-id="ec1b1-119">'T</span></span>

<span data-ttu-id="ec1b1-120">Der Eingabetyp des Vorgangs, der verzögert werden soll.</span><span class="sxs-lookup"><span data-stu-id="ec1b1-120">The input type of the operation to be delayed.</span></span>

## <a name="see-also"></a><span data-ttu-id="ec1b1-121">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ec1b1-121">See Also</span></span>

- [<span data-ttu-id="ec1b1-122">Microsoft. Quantum. Canon. Delay</span><span class="sxs-lookup"><span data-stu-id="ec1b1-122">Microsoft.Quantum.Canon.Delay</span></span>](xref:Microsoft.Quantum.Canon.Delay)
- [<span data-ttu-id="ec1b1-123">Microsoft. Quantum. Canon. verzögert</span><span class="sxs-lookup"><span data-stu-id="ec1b1-123">Microsoft.Quantum.Canon.Delayed</span></span>](xref:Microsoft.Quantum.Canon.Delayed)