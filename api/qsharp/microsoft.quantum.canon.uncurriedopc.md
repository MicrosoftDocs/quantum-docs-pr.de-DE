---
uid: Microsoft.Quantum.Canon.UncurriedOpC
title: Uncurriedopc-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: UncurriedOpC
qsharp.summary: Given a function which returns operations, returns a new operation which takes both inputs as a tuple. The modifier `C` indicates that the operations are controllable.
ms.openlocfilehash: f3e5ecf3f7df0393dfbb948f064c27505f04cfcf
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703715"
---
# <a name="uncurriedopc-function"></a><span data-ttu-id="b324d-102">Uncurriedopc-Funktion</span><span class="sxs-lookup"><span data-stu-id="b324d-102">UncurriedOpC function</span></span>

<span data-ttu-id="b324d-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="b324d-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="b324d-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="b324d-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="b324d-105">Gibt eine Funktion zurück, die Vorgänge zurückgibt, gibt einen neuen Vorgang zurück, der beide Eingaben als Tupel annimmt.</span><span class="sxs-lookup"><span data-stu-id="b324d-105">Given a function which returns operations, returns a new operation which takes both inputs as a tuple.</span></span>
<span data-ttu-id="b324d-106">Der-Modifizierer `C` gibt an, dass die Vorgänge steuerbar sind.</span><span class="sxs-lookup"><span data-stu-id="b324d-106">The modifier `C` indicates that the operations are controllable.</span></span>

```qsharp
function UncurriedOpC<'T, 'U> (curriedOp : ('T -> ('U => Unit is Ctl))) : (('T, 'U) => Unit is Ctl)
```


## <a name="input"></a><span data-ttu-id="b324d-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b324d-107">Input</span></span>

### <a name="curriedop--t---u--unit-ctl"></a><span data-ttu-id="b324d-108">curriedop: 't-> ' U => [Unit](xref:microsoft.quantum.lang-ref.unit) CTL</span><span class="sxs-lookup"><span data-stu-id="b324d-108">curriedOp : 'T -> 'U => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>

<span data-ttu-id="b324d-109">Eine Funktion, die Vorgänge zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="b324d-109">A function which returns operations.</span></span>



## <a name="output--tu--unit-ctl"></a><span data-ttu-id="b324d-110">Ausgabe: ('t, ' U) => [Unit](xref:microsoft.quantum.lang-ref.unit) CTL</span><span class="sxs-lookup"><span data-stu-id="b324d-110">Output : ('T,'U) => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>

<span data-ttu-id="b324d-111">Ein neuer Vorgang `op` , der `op(t, u)` entspricht `(curriedOp(t))(u)` .</span><span class="sxs-lookup"><span data-stu-id="b324d-111">A new operation `op` such that `op(t, u)` is equivalent to `(curriedOp(t))(u)`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="b324d-112">Typparameter</span><span class="sxs-lookup"><span data-stu-id="b324d-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="b324d-113">GIF</span><span class="sxs-lookup"><span data-stu-id="b324d-113">'T</span></span>

<span data-ttu-id="b324d-114">Der Typ des ersten Arguments einer Curry-Funktion.</span><span class="sxs-lookup"><span data-stu-id="b324d-114">The type of the first argument of a curried function.</span></span>
### <a name="u"></a><span data-ttu-id="b324d-115">"U</span><span class="sxs-lookup"><span data-stu-id="b324d-115">'U</span></span>

<span data-ttu-id="b324d-116">Der Typ des zweiten Arguments einer Curry-Funktion.</span><span class="sxs-lookup"><span data-stu-id="b324d-116">The type of the second argument of a curried function.</span></span>

## <a name="see-also"></a><span data-ttu-id="b324d-117">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b324d-117">See Also</span></span>

- [<span data-ttu-id="b324d-118">Microsoft. Quantum. Canon. uncurriedop</span><span class="sxs-lookup"><span data-stu-id="b324d-118">Microsoft.Quantum.Canon.UncurriedOp</span></span>](xref:Microsoft.Quantum.Canon.UncurriedOp)