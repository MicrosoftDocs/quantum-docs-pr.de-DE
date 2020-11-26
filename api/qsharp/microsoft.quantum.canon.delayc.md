---
uid: Microsoft.Quantum.Canon.DelayC
title: Delta-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: DelayC
qsharp.summary: Applies a given operation with a delay.
ms.openlocfilehash: 7a11c3990802ff36856a90de927b38d2ede8bd9d
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96216488"
---
# <a name="delayc-operation"></a><span data-ttu-id="7d666-102">Delta-Vorgang</span><span class="sxs-lookup"><span data-stu-id="7d666-102">DelayC operation</span></span>

<span data-ttu-id="7d666-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="7d666-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="7d666-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="7d666-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="7d666-105">Wendet einen angegebenen Vorgang mit einer Verzögerung an.</span><span class="sxs-lookup"><span data-stu-id="7d666-105">Applies a given operation with a delay.</span></span>

```qsharp
operation DelayC<'T> (op : ('T => Unit is Ctl), arg : 'T, aux : Unit) : Unit is Ctl
```


## <a name="description"></a><span data-ttu-id="7d666-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7d666-106">Description</span></span>

<span data-ttu-id="7d666-107">Wenn ein Vorgang und eine Eingabe für diesen Vorgang vorhanden sind, wendet den Vorgang an, sobald eine zusätzliche Eingabe bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="7d666-107">Given an operation and an input to that operation, applies the operation once an additional input is provided.</span></span>
<span data-ttu-id="7d666-108">Der-Ausdruck ist insbesondere `Delay(op, arg, _)` ein Vorgang, der `op` sich auf bezieht, `arg` Wenn aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="7d666-108">In particular, the expression `Delay(op, arg, _)` is an operation that applies `op` to `arg` when called.</span></span>
<span data-ttu-id="7d666-109">`Delay(op,arg,_)`Der Ausdruck ermöglicht das Verzögern der Anwendung von `op` .</span><span class="sxs-lookup"><span data-stu-id="7d666-109">Expression `Delay(op,arg,_)` allows to delay the application of `op`.</span></span>

## <a name="input"></a><span data-ttu-id="7d666-110">Eingabe</span><span class="sxs-lookup"><span data-stu-id="7d666-110">Input</span></span>

### <a name="op--t--unit--is-ctl"></a><span data-ttu-id="7d666-111">OP: 't => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist CTL</span><span class="sxs-lookup"><span data-stu-id="7d666-111">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="7d666-112">Ein anzuwendende Vorgang.</span><span class="sxs-lookup"><span data-stu-id="7d666-112">An operation to be applied.</span></span>


### <a name="arg--t"></a><span data-ttu-id="7d666-113">arg: 't</span><span class="sxs-lookup"><span data-stu-id="7d666-113">arg : 'T</span></span>

<span data-ttu-id="7d666-114">Die Eingabe, auf die der Vorgang angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="7d666-114">The input to which the operation is applied.</span></span>


### <a name="aux--unit"></a><span data-ttu-id="7d666-115">AUX: [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="7d666-115">aux : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

<span data-ttu-id="7d666-116">Argument, das verwendet wird, um die Anwendung des Vorgangs mithilfe der partiellen Anwendung zu verzögern.</span><span class="sxs-lookup"><span data-stu-id="7d666-116">Argument used to delay the application of operation by using partial application.</span></span>



## <a name="output--unit"></a><span data-ttu-id="7d666-117">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="7d666-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="7d666-118">Typparameter</span><span class="sxs-lookup"><span data-stu-id="7d666-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="7d666-119">GIF</span><span class="sxs-lookup"><span data-stu-id="7d666-119">'T</span></span>

<span data-ttu-id="7d666-120">Der Eingabetyp des Vorgangs, der verzögert werden soll.</span><span class="sxs-lookup"><span data-stu-id="7d666-120">The input type of the operation to be delayed.</span></span>

## <a name="see-also"></a><span data-ttu-id="7d666-121">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="7d666-121">See Also</span></span>

- [<span data-ttu-id="7d666-122">Microsoft. Quantum. Canon. Delay</span><span class="sxs-lookup"><span data-stu-id="7d666-122">Microsoft.Quantum.Canon.Delay</span></span>](xref:Microsoft.Quantum.Canon.Delay)
- [<span data-ttu-id="7d666-123">Microsoft. Quantum. Canon. verzögert</span><span class="sxs-lookup"><span data-stu-id="7d666-123">Microsoft.Quantum.Canon.Delayed</span></span>](xref:Microsoft.Quantum.Canon.Delayed)