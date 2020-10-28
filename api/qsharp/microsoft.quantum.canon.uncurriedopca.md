---
uid: Microsoft.Quantum.Canon.UncurriedOpCA
title: Uncurriedopca-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: UncurriedOpCA
qsharp.summary: Given a function which returns operations, returns a new operation which takes both inputs as a tuple. The modifier `CA` indicates that the operations are controllable and adjointable.
ms.openlocfilehash: 6a0f2e1b345d0ba3ac5c779c5dc2bfffaf659a0b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703710"
---
# <a name="uncurriedopca-function"></a><span data-ttu-id="868cd-102">Uncurriedopca-Funktion</span><span class="sxs-lookup"><span data-stu-id="868cd-102">UncurriedOpCA function</span></span>

<span data-ttu-id="868cd-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="868cd-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="868cd-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="868cd-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="868cd-105">Gibt eine Funktion zurück, die Vorgänge zurückgibt, gibt einen neuen Vorgang zurück, der beide Eingaben als Tupel annimmt.</span><span class="sxs-lookup"><span data-stu-id="868cd-105">Given a function which returns operations, returns a new operation which takes both inputs as a tuple.</span></span>
<span data-ttu-id="868cd-106">Der-Modifizierer `CA` gibt an, dass die Vorgänge steuerbar und adjointable sind.</span><span class="sxs-lookup"><span data-stu-id="868cd-106">The modifier `CA` indicates that the operations are controllable and adjointable.</span></span>

```qsharp
function UncurriedOpCA<'T, 'U> (curriedOp : ('T -> ('U => Unit is Ctl + Adj))) : (('T, 'U) => Unit is Ctl + Adj)
```


## <a name="input"></a><span data-ttu-id="868cd-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="868cd-107">Input</span></span>

### <a name="curriedop--t---u--unit-ctl--adj"></a><span data-ttu-id="868cd-108">curriedop: 't-> ' U => [Unit](xref:microsoft.quantum.lang-ref.unit) CTL + ADJ</span><span class="sxs-lookup"><span data-stu-id="868cd-108">curriedOp : 'T -> 'U => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl + Adj</span></span>

<span data-ttu-id="868cd-109">Eine Funktion, die Vorgänge zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="868cd-109">A function which returns operations.</span></span>



## <a name="output--tu--unit-ctl--adj"></a><span data-ttu-id="868cd-110">Ausgabe: ('t, ' U) => [Unit](xref:microsoft.quantum.lang-ref.unit) CTL + ADJ</span><span class="sxs-lookup"><span data-stu-id="868cd-110">Output : ('T,'U) => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl + Adj</span></span>

<span data-ttu-id="868cd-111">Ein neuer Vorgang `op` , der `op(t, u)` entspricht `(curriedOp(t))(u)` .</span><span class="sxs-lookup"><span data-stu-id="868cd-111">A new operation `op` such that `op(t, u)` is equivalent to `(curriedOp(t))(u)`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="868cd-112">Typparameter</span><span class="sxs-lookup"><span data-stu-id="868cd-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="868cd-113">GIF</span><span class="sxs-lookup"><span data-stu-id="868cd-113">'T</span></span>

<span data-ttu-id="868cd-114">Der Typ des ersten Arguments einer Curry-Funktion.</span><span class="sxs-lookup"><span data-stu-id="868cd-114">The type of the first argument of a curried function.</span></span>
### <a name="u"></a><span data-ttu-id="868cd-115">"U</span><span class="sxs-lookup"><span data-stu-id="868cd-115">'U</span></span>

<span data-ttu-id="868cd-116">Der Typ des zweiten Arguments einer Curry-Funktion.</span><span class="sxs-lookup"><span data-stu-id="868cd-116">The type of the second argument of a curried function.</span></span>

## <a name="see-also"></a><span data-ttu-id="868cd-117">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="868cd-117">See Also</span></span>

- [<span data-ttu-id="868cd-118">Microsoft. Quantum. Canon. uncurriedop</span><span class="sxs-lookup"><span data-stu-id="868cd-118">Microsoft.Quantum.Canon.UncurriedOp</span></span>](xref:Microsoft.Quantum.Canon.UncurriedOp)