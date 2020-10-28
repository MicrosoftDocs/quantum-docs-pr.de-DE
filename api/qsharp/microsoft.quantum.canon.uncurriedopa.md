---
uid: Microsoft.Quantum.Canon.UncurriedOpA
title: Uncurriedopa-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: UncurriedOpA
qsharp.summary: Given a function which returns operations, returns a new operation which takes both inputs as a tuple. The modifier `A` indicates that the operations are adjointable.
ms.openlocfilehash: 21df20354ad2388891f32b1bf1c7781287904983
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703716"
---
# <a name="uncurriedopa-function"></a><span data-ttu-id="ad75c-102">Uncurriedopa-Funktion</span><span class="sxs-lookup"><span data-stu-id="ad75c-102">UncurriedOpA function</span></span>

<span data-ttu-id="ad75c-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="ad75c-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="ad75c-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="ad75c-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="ad75c-105">Gibt eine Funktion zurück, die Vorgänge zurückgibt, gibt einen neuen Vorgang zurück, der beide Eingaben als Tupel annimmt.</span><span class="sxs-lookup"><span data-stu-id="ad75c-105">Given a function which returns operations, returns a new operation which takes both inputs as a tuple.</span></span>
<span data-ttu-id="ad75c-106">Der-Modifizierer `A` gibt an, dass die Vorgänge adjointable sind.</span><span class="sxs-lookup"><span data-stu-id="ad75c-106">The modifier `A` indicates that the operations are adjointable.</span></span>

```qsharp
function UncurriedOpA<'T, 'U> (curriedOp : ('T -> ('U => Unit is Adj))) : (('T, 'U) => Unit is Adj)
```


## <a name="input"></a><span data-ttu-id="ad75c-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ad75c-107">Input</span></span>

### <a name="curriedop--t---u--unit-adj"></a><span data-ttu-id="ad75c-108">curriedop: 't-> ' U => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ</span><span class="sxs-lookup"><span data-stu-id="ad75c-108">curriedOp : 'T -> 'U => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="ad75c-109">Eine Funktion, die Vorgänge zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="ad75c-109">A function which returns operations.</span></span>



## <a name="output--tu--unit-adj"></a><span data-ttu-id="ad75c-110">Ausgabe: ('t, ' U) => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ</span><span class="sxs-lookup"><span data-stu-id="ad75c-110">Output : ('T,'U) => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="ad75c-111">Ein neuer Vorgang `op` , der `op(t, u)` entspricht `(curriedOp(t))(u)` .</span><span class="sxs-lookup"><span data-stu-id="ad75c-111">A new operation `op` such that `op(t, u)` is equivalent to `(curriedOp(t))(u)`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="ad75c-112">Typparameter</span><span class="sxs-lookup"><span data-stu-id="ad75c-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="ad75c-113">GIF</span><span class="sxs-lookup"><span data-stu-id="ad75c-113">'T</span></span>

<span data-ttu-id="ad75c-114">Der Typ des ersten Arguments einer Curry-Funktion.</span><span class="sxs-lookup"><span data-stu-id="ad75c-114">The type of the first argument of a curried function.</span></span>
### <a name="u"></a><span data-ttu-id="ad75c-115">"U</span><span class="sxs-lookup"><span data-stu-id="ad75c-115">'U</span></span>

<span data-ttu-id="ad75c-116">Der Typ des zweiten Arguments einer Curry-Funktion.</span><span class="sxs-lookup"><span data-stu-id="ad75c-116">The type of the second argument of a curried function.</span></span>

## <a name="see-also"></a><span data-ttu-id="ad75c-117">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ad75c-117">See Also</span></span>

- [<span data-ttu-id="ad75c-118">Microsoft. Quantum. Canon. uncurriedop</span><span class="sxs-lookup"><span data-stu-id="ad75c-118">Microsoft.Quantum.Canon.UncurriedOp</span></span>](xref:Microsoft.Quantum.Canon.UncurriedOp)