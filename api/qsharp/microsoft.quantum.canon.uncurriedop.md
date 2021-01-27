---
uid: Microsoft.Quantum.Canon.UncurriedOp
title: Uncurriedop-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: UncurriedOp
qsharp.summary: Given a function which returns operations, returns a new operation which takes both inputs as a tuple.
ms.openlocfilehash: d707b52bb17f4dea795fa4ff824c785e506b8b20
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98852005"
---
# <a name="uncurriedop-function"></a><span data-ttu-id="b47fe-102">Uncurriedop-Funktion</span><span class="sxs-lookup"><span data-stu-id="b47fe-102">UncurriedOp function</span></span>

<span data-ttu-id="b47fe-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="b47fe-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="b47fe-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="b47fe-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="b47fe-105">Gibt eine Funktion zurück, die Vorgänge zurückgibt, gibt einen neuen Vorgang zurück, der beide Eingaben als Tupel annimmt.</span><span class="sxs-lookup"><span data-stu-id="b47fe-105">Given a function which returns operations, returns a new operation which takes both inputs as a tuple.</span></span>

```qsharp
function UncurriedOp<'T, 'U> (curriedOp : ('T -> ('U => Unit))) : (('T, 'U) => Unit)
```


## <a name="input"></a><span data-ttu-id="b47fe-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b47fe-106">Input</span></span>

### <a name="curriedop--t---u--unit"></a><span data-ttu-id="b47fe-107">curriedop: 't-> ' U => [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="b47fe-107">curriedOp : 'T -> 'U => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="b47fe-108">Eine Funktion, die Vorgänge zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="b47fe-108">A function which returns operations.</span></span>



## <a name="output--tu--unit"></a><span data-ttu-id="b47fe-109">Ausgabe: ('t, ' U) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="b47fe-109">Output : ('T,'U) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="b47fe-110">Ein neuer Vorgang `op` , der `op(t, u)` entspricht `(curriedOp(t))(u)` .</span><span class="sxs-lookup"><span data-stu-id="b47fe-110">A new operation `op` such that `op(t, u)` is equivalent to `(curriedOp(t))(u)`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="b47fe-111">Typparameter</span><span class="sxs-lookup"><span data-stu-id="b47fe-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="b47fe-112">GIF</span><span class="sxs-lookup"><span data-stu-id="b47fe-112">'T</span></span>

<span data-ttu-id="b47fe-113">Der Typ der ersten Eingabe für einen geschweifenden Vorgang.</span><span class="sxs-lookup"><span data-stu-id="b47fe-113">The type of the first input to a curried operation.</span></span>
### <a name="u"></a><span data-ttu-id="b47fe-114">"U</span><span class="sxs-lookup"><span data-stu-id="b47fe-114">'U</span></span>

<span data-ttu-id="b47fe-115">Der Typ der zweiten Eingabe für einen geschweifenden Vorgang.</span><span class="sxs-lookup"><span data-stu-id="b47fe-115">The type of the second input to a curried operation.</span></span>

## <a name="see-also"></a><span data-ttu-id="b47fe-116">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b47fe-116">See Also</span></span>

- [<span data-ttu-id="b47fe-117">Microsoft. Quantum. Canon. uncurriedopc</span><span class="sxs-lookup"><span data-stu-id="b47fe-117">Microsoft.Quantum.Canon.UncurriedOpC</span></span>](xref:Microsoft.Quantum.Canon.UncurriedOpC)
- [<span data-ttu-id="b47fe-118">Microsoft. Quantum. Canon. uncurriedopa</span><span class="sxs-lookup"><span data-stu-id="b47fe-118">Microsoft.Quantum.Canon.UncurriedOpA</span></span>](xref:Microsoft.Quantum.Canon.UncurriedOpA)
- [<span data-ttu-id="b47fe-119">Microsoft. Quantum. Canon. uncurriedopca</span><span class="sxs-lookup"><span data-stu-id="b47fe-119">Microsoft.Quantum.Canon.UncurriedOpCA</span></span>](xref:Microsoft.Quantum.Canon.UncurriedOpCA)