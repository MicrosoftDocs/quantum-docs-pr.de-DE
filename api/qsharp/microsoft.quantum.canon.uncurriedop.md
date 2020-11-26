---
uid: Microsoft.Quantum.Canon.UncurriedOp
title: Uncurriedop-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: UncurriedOp
qsharp.summary: Given a function which returns operations, returns a new operation which takes both inputs as a tuple.
ms.openlocfilehash: cad508f166d4af805cb98cd21a0260d9babb6a4c
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96204639"
---
# <a name="uncurriedop-function"></a><span data-ttu-id="b2621-102">Uncurriedop-Funktion</span><span class="sxs-lookup"><span data-stu-id="b2621-102">UncurriedOp function</span></span>

<span data-ttu-id="b2621-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="b2621-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="b2621-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="b2621-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="b2621-105">Gibt eine Funktion zurück, die Vorgänge zurückgibt, gibt einen neuen Vorgang zurück, der beide Eingaben als Tupel annimmt.</span><span class="sxs-lookup"><span data-stu-id="b2621-105">Given a function which returns operations, returns a new operation which takes both inputs as a tuple.</span></span>

```qsharp
function UncurriedOp<'T, 'U> (curriedOp : ('T -> ('U => Unit))) : (('T, 'U) => Unit)
```


## <a name="input"></a><span data-ttu-id="b2621-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b2621-106">Input</span></span>

### <a name="curriedop--t---u--unit"></a><span data-ttu-id="b2621-107">curriedop: 't-> ' U => [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="b2621-107">curriedOp : 'T -> 'U => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="b2621-108">Eine Funktion, die Vorgänge zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="b2621-108">A function which returns operations.</span></span>



## <a name="output--tu--unit"></a><span data-ttu-id="b2621-109">Ausgabe: ('t, ' U) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="b2621-109">Output : ('T,'U) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="b2621-110">Ein neuer Vorgang `op` , der `op(t, u)` entspricht `(curriedOp(t))(u)` .</span><span class="sxs-lookup"><span data-stu-id="b2621-110">A new operation `op` such that `op(t, u)` is equivalent to `(curriedOp(t))(u)`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="b2621-111">Typparameter</span><span class="sxs-lookup"><span data-stu-id="b2621-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="b2621-112">GIF</span><span class="sxs-lookup"><span data-stu-id="b2621-112">'T</span></span>

<span data-ttu-id="b2621-113">Der Typ der ersten Eingabe für einen geschweifenden Vorgang.</span><span class="sxs-lookup"><span data-stu-id="b2621-113">The type of the first input to a curried operation.</span></span>
### <a name="u"></a><span data-ttu-id="b2621-114">"U</span><span class="sxs-lookup"><span data-stu-id="b2621-114">'U</span></span>

<span data-ttu-id="b2621-115">Der Typ der zweiten Eingabe für einen geschweifenden Vorgang.</span><span class="sxs-lookup"><span data-stu-id="b2621-115">The type of the second input to a curried operation.</span></span>

## <a name="see-also"></a><span data-ttu-id="b2621-116">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b2621-116">See Also</span></span>

- [<span data-ttu-id="b2621-117">Microsoft. Quantum. Canon. uncurriedopc</span><span class="sxs-lookup"><span data-stu-id="b2621-117">Microsoft.Quantum.Canon.UncurriedOpC</span></span>](xref:Microsoft.Quantum.Canon.UncurriedOpC)
- [<span data-ttu-id="b2621-118">Microsoft. Quantum. Canon. uncurriedopa</span><span class="sxs-lookup"><span data-stu-id="b2621-118">Microsoft.Quantum.Canon.UncurriedOpA</span></span>](xref:Microsoft.Quantum.Canon.UncurriedOpA)
- [<span data-ttu-id="b2621-119">Microsoft. Quantum. Canon. uncurriedopca</span><span class="sxs-lookup"><span data-stu-id="b2621-119">Microsoft.Quantum.Canon.UncurriedOpCA</span></span>](xref:Microsoft.Quantum.Canon.UncurriedOpCA)