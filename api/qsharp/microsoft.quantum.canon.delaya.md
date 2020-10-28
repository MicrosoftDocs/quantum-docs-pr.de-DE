---
uid: Microsoft.Quantum.Canon.DelayA
title: Delaya-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: DelayA
qsharp.summary: Applies a given operation with a delay.
ms.openlocfilehash: 77c40633824ccd9250252804b08d7400936515dd
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704242"
---
# <a name="delaya-operation"></a><span data-ttu-id="deeff-102">Delaya-Vorgang</span><span class="sxs-lookup"><span data-stu-id="deeff-102">DelayA operation</span></span>

<span data-ttu-id="deeff-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="deeff-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="deeff-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="deeff-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="deeff-105">Wendet einen angegebenen Vorgang mit einer Verzögerung an.</span><span class="sxs-lookup"><span data-stu-id="deeff-105">Applies a given operation with a delay.</span></span>

```qsharp
operation DelayA<'T> (op : ('T => Unit is Adj), arg : 'T, aux : Unit) : Unit
```


## <a name="description"></a><span data-ttu-id="deeff-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="deeff-106">Description</span></span>

<span data-ttu-id="deeff-107">Wenn ein Vorgang und eine Eingabe für diesen Vorgang vorhanden sind, wendet den Vorgang an, sobald eine zusätzliche Eingabe bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="deeff-107">Given an operation and an input to that operation, applies the operation once an additional input is provided.</span></span>
<span data-ttu-id="deeff-108">Der-Ausdruck ist insbesondere `Delay(op, arg, _)` ein Vorgang, der `op` sich auf bezieht, `arg` Wenn aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="deeff-108">In particular, the expression `Delay(op, arg, _)` is an operation that applies `op` to `arg` when called.</span></span>
<span data-ttu-id="deeff-109">`Delay(op,arg,_)`Der Ausdruck ermöglicht das Verzögern der Anwendung von `op` .</span><span class="sxs-lookup"><span data-stu-id="deeff-109">Expression `Delay(op,arg,_)` allows to delay the application of `op`.</span></span>

## <a name="input"></a><span data-ttu-id="deeff-110">Eingabe</span><span class="sxs-lookup"><span data-stu-id="deeff-110">Input</span></span>

### <a name="op--t--unit-adj"></a><span data-ttu-id="deeff-111">OP: 't => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ</span><span class="sxs-lookup"><span data-stu-id="deeff-111">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="deeff-112">Ein anzuwendende Vorgang.</span><span class="sxs-lookup"><span data-stu-id="deeff-112">An operation to be applied.</span></span>


### <a name="arg--t"></a><span data-ttu-id="deeff-113">arg: 't</span><span class="sxs-lookup"><span data-stu-id="deeff-113">arg : 'T</span></span>

<span data-ttu-id="deeff-114">Die Eingabe, auf die der Vorgang angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="deeff-114">The input to which the operation is applied.</span></span>


### <a name="aux--unit"></a><span data-ttu-id="deeff-115">AUX: [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="deeff-115">aux : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

<span data-ttu-id="deeff-116">Argument, das verwendet wird, um die Anwendung des Vorgangs mithilfe der partiellen Anwendung zu verzögern.</span><span class="sxs-lookup"><span data-stu-id="deeff-116">Argument used to delay the application of operation by using partial application.</span></span>



## <a name="output--unit"></a><span data-ttu-id="deeff-117">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="deeff-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="deeff-118">Typparameter</span><span class="sxs-lookup"><span data-stu-id="deeff-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="deeff-119">GIF</span><span class="sxs-lookup"><span data-stu-id="deeff-119">'T</span></span>

<span data-ttu-id="deeff-120">Der Eingabetyp des Vorgangs, der verzögert werden soll.</span><span class="sxs-lookup"><span data-stu-id="deeff-120">The input type of the operation to be delayed.</span></span>

## <a name="see-also"></a><span data-ttu-id="deeff-121">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="deeff-121">See Also</span></span>

- [<span data-ttu-id="deeff-122">Microsoft. Quantum. Canon. Delay</span><span class="sxs-lookup"><span data-stu-id="deeff-122">Microsoft.Quantum.Canon.Delay</span></span>](xref:Microsoft.Quantum.Canon.Delay)
- [<span data-ttu-id="deeff-123">Microsoft. Quantum. Canon. verzögert</span><span class="sxs-lookup"><span data-stu-id="deeff-123">Microsoft.Quantum.Canon.Delayed</span></span>](xref:Microsoft.Quantum.Canon.Delayed)