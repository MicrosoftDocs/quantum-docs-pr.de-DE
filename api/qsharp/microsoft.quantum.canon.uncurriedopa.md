---
uid: Microsoft.Quantum.Canon.UncurriedOpA
title: Uncurriedopa-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: UncurriedOpA
qsharp.summary: Given a function which returns operations, returns a new operation which takes both inputs as a tuple. The modifier `A` indicates that the operations are adjointable.
ms.openlocfilehash: e535d017d2665ddb76e5f422e18b8656c73171c6
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96204622"
---
# <a name="uncurriedopa-function"></a><span data-ttu-id="e5146-102">Uncurriedopa-Funktion</span><span class="sxs-lookup"><span data-stu-id="e5146-102">UncurriedOpA function</span></span>

<span data-ttu-id="e5146-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="e5146-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="e5146-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="e5146-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="e5146-105">Gibt eine Funktion zurück, die Vorgänge zurückgibt, gibt einen neuen Vorgang zurück, der beide Eingaben als Tupel annimmt.</span><span class="sxs-lookup"><span data-stu-id="e5146-105">Given a function which returns operations, returns a new operation which takes both inputs as a tuple.</span></span>
<span data-ttu-id="e5146-106">Der-Modifizierer `A` gibt an, dass die Vorgänge adjointable sind.</span><span class="sxs-lookup"><span data-stu-id="e5146-106">The modifier `A` indicates that the operations are adjointable.</span></span>

```qsharp
function UncurriedOpA<'T, 'U> (curriedOp : ('T -> ('U => Unit is Adj))) : (('T, 'U) => Unit is Adj)
```


## <a name="input"></a><span data-ttu-id="e5146-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e5146-107">Input</span></span>

### <a name="curriedop--t---u--unit--is-adj"></a><span data-ttu-id="e5146-108">curriedop: 't-> ' U => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ</span><span class="sxs-lookup"><span data-stu-id="e5146-108">curriedOp : 'T -> 'U => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="e5146-109">Eine Funktion, die Vorgänge zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="e5146-109">A function which returns operations.</span></span>



## <a name="output--tu--unit--is-adj"></a><span data-ttu-id="e5146-110">Ausgabe: ('t, ' U) => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ</span><span class="sxs-lookup"><span data-stu-id="e5146-110">Output : ('T,'U) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="e5146-111">Ein neuer Vorgang `op` , der `op(t, u)` entspricht `(curriedOp(t))(u)` .</span><span class="sxs-lookup"><span data-stu-id="e5146-111">A new operation `op` such that `op(t, u)` is equivalent to `(curriedOp(t))(u)`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="e5146-112">Typparameter</span><span class="sxs-lookup"><span data-stu-id="e5146-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="e5146-113">GIF</span><span class="sxs-lookup"><span data-stu-id="e5146-113">'T</span></span>

<span data-ttu-id="e5146-114">Der Typ des ersten Arguments einer Curry-Funktion.</span><span class="sxs-lookup"><span data-stu-id="e5146-114">The type of the first argument of a curried function.</span></span>
### <a name="u"></a><span data-ttu-id="e5146-115">"U</span><span class="sxs-lookup"><span data-stu-id="e5146-115">'U</span></span>

<span data-ttu-id="e5146-116">Der Typ des zweiten Arguments einer Curry-Funktion.</span><span class="sxs-lookup"><span data-stu-id="e5146-116">The type of the second argument of a curried function.</span></span>

## <a name="see-also"></a><span data-ttu-id="e5146-117">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e5146-117">See Also</span></span>

- [<span data-ttu-id="e5146-118">Microsoft. Quantum. Canon. uncurriedop</span><span class="sxs-lookup"><span data-stu-id="e5146-118">Microsoft.Quantum.Canon.UncurriedOp</span></span>](xref:Microsoft.Quantum.Canon.UncurriedOp)