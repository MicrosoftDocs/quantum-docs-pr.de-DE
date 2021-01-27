---
uid: Microsoft.Quantum.Canon.DelayCA
title: Delta-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: DelayCA
qsharp.summary: Applies a given operation with a delay.
ms.openlocfilehash: a8606cde976882bba0eb23467932b9ee0ed36696
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840622"
---
# <a name="delayca-operation"></a><span data-ttu-id="8f2ba-102">Delta-Vorgang</span><span class="sxs-lookup"><span data-stu-id="8f2ba-102">DelayCA operation</span></span>

<span data-ttu-id="8f2ba-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="8f2ba-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="8f2ba-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="8f2ba-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="8f2ba-105">Wendet einen angegebenen Vorgang mit einer Verzögerung an.</span><span class="sxs-lookup"><span data-stu-id="8f2ba-105">Applies a given operation with a delay.</span></span>

```qsharp
operation DelayCA<'T> (op : ('T => Unit is Ctl + Adj), arg : 'T, aux : Unit) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="8f2ba-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8f2ba-106">Description</span></span>

<span data-ttu-id="8f2ba-107">Wenn ein Vorgang und eine Eingabe für diesen Vorgang vorhanden sind, wendet den Vorgang an, sobald eine zusätzliche Eingabe bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="8f2ba-107">Given an operation and an input to that operation, applies the operation once an additional input is provided.</span></span>
<span data-ttu-id="8f2ba-108">Der-Ausdruck ist insbesondere `Delay(op, arg, _)` ein Vorgang, der `op` sich auf bezieht, `arg` Wenn aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="8f2ba-108">In particular, the expression `Delay(op, arg, _)` is an operation that applies `op` to `arg` when called.</span></span>
<span data-ttu-id="8f2ba-109">`Delay(op,arg,_)`Der Ausdruck ermöglicht das Verzögern der Anwendung von `op` .</span><span class="sxs-lookup"><span data-stu-id="8f2ba-109">Expression `Delay(op,arg,_)` allows to delay the application of `op`.</span></span>

## <a name="input"></a><span data-ttu-id="8f2ba-110">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8f2ba-110">Input</span></span>

### <a name="op--t--unit--is-adj--ctl"></a><span data-ttu-id="8f2ba-111">OP: 't => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="8f2ba-111">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="8f2ba-112">Ein anzuwendende Vorgang.</span><span class="sxs-lookup"><span data-stu-id="8f2ba-112">An operation to be applied.</span></span>


### <a name="arg--t"></a><span data-ttu-id="8f2ba-113">arg: 't</span><span class="sxs-lookup"><span data-stu-id="8f2ba-113">arg : 'T</span></span>

<span data-ttu-id="8f2ba-114">Die Eingabe, auf die der Vorgang angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="8f2ba-114">The input to which the operation is applied.</span></span>


### <a name="aux--unit"></a><span data-ttu-id="8f2ba-115">AUX: [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="8f2ba-115">aux : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

<span data-ttu-id="8f2ba-116">Argument, das verwendet wird, um die Anwendung des Vorgangs mithilfe der partiellen Anwendung zu verzögern.</span><span class="sxs-lookup"><span data-stu-id="8f2ba-116">Argument used to delay the application of operation by using partial application.</span></span>



## <a name="output--unit"></a><span data-ttu-id="8f2ba-117">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="8f2ba-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="8f2ba-118">Typparameter</span><span class="sxs-lookup"><span data-stu-id="8f2ba-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="8f2ba-119">GIF</span><span class="sxs-lookup"><span data-stu-id="8f2ba-119">'T</span></span>

<span data-ttu-id="8f2ba-120">Der Eingabetyp des Vorgangs, der verzögert werden soll.</span><span class="sxs-lookup"><span data-stu-id="8f2ba-120">The input type of the operation to be delayed.</span></span>

## <a name="see-also"></a><span data-ttu-id="8f2ba-121">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="8f2ba-121">See Also</span></span>

- [<span data-ttu-id="8f2ba-122">Microsoft. Quantum. Canon. Delay</span><span class="sxs-lookup"><span data-stu-id="8f2ba-122">Microsoft.Quantum.Canon.Delay</span></span>](xref:Microsoft.Quantum.Canon.Delay)
- [<span data-ttu-id="8f2ba-123">Microsoft. Quantum. Canon. verzögert</span><span class="sxs-lookup"><span data-stu-id="8f2ba-123">Microsoft.Quantum.Canon.Delayed</span></span>](xref:Microsoft.Quantum.Canon.Delayed)