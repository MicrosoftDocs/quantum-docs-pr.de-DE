---
uid: Microsoft.Quantum.Canon.UncurriedOpCA
title: Uncurriedopca-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: UncurriedOpCA
qsharp.summary: Given a function which returns operations, returns a new operation which takes both inputs as a tuple. The modifier `CA` indicates that the operations are controllable and adjointable.
ms.openlocfilehash: 45526c0202e417213aab3fe7819827588e794e23
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96216386"
---
# <a name="uncurriedopca-function"></a><span data-ttu-id="63eba-102">Uncurriedopca-Funktion</span><span class="sxs-lookup"><span data-stu-id="63eba-102">UncurriedOpCA function</span></span>

<span data-ttu-id="63eba-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="63eba-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="63eba-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="63eba-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="63eba-105">Gibt eine Funktion zurück, die Vorgänge zurückgibt, gibt einen neuen Vorgang zurück, der beide Eingaben als Tupel annimmt.</span><span class="sxs-lookup"><span data-stu-id="63eba-105">Given a function which returns operations, returns a new operation which takes both inputs as a tuple.</span></span>
<span data-ttu-id="63eba-106">Der-Modifizierer `CA` gibt an, dass die Vorgänge steuerbar und adjointable sind.</span><span class="sxs-lookup"><span data-stu-id="63eba-106">The modifier `CA` indicates that the operations are controllable and adjointable.</span></span>

```qsharp
function UncurriedOpCA<'T, 'U> (curriedOp : ('T -> ('U => Unit is Ctl + Adj))) : (('T, 'U) => Unit is Ctl + Adj)
```


## <a name="input"></a><span data-ttu-id="63eba-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="63eba-107">Input</span></span>

### <a name="curriedop--t---u--unit--is-adj--ctl"></a><span data-ttu-id="63eba-108">curriedop: 't-> ' U => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="63eba-108">curriedOp : 'T -> 'U => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="63eba-109">Eine Funktion, die Vorgänge zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="63eba-109">A function which returns operations.</span></span>



## <a name="output--tu--unit--is-adj--ctl"></a><span data-ttu-id="63eba-110">Ausgabe: ('t, ' U) => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="63eba-110">Output : ('T,'U) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="63eba-111">Ein neuer Vorgang `op` , der `op(t, u)` entspricht `(curriedOp(t))(u)` .</span><span class="sxs-lookup"><span data-stu-id="63eba-111">A new operation `op` such that `op(t, u)` is equivalent to `(curriedOp(t))(u)`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="63eba-112">Typparameter</span><span class="sxs-lookup"><span data-stu-id="63eba-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="63eba-113">GIF</span><span class="sxs-lookup"><span data-stu-id="63eba-113">'T</span></span>

<span data-ttu-id="63eba-114">Der Typ des ersten Arguments einer Curry-Funktion.</span><span class="sxs-lookup"><span data-stu-id="63eba-114">The type of the first argument of a curried function.</span></span>
### <a name="u"></a><span data-ttu-id="63eba-115">"U</span><span class="sxs-lookup"><span data-stu-id="63eba-115">'U</span></span>

<span data-ttu-id="63eba-116">Der Typ des zweiten Arguments einer Curry-Funktion.</span><span class="sxs-lookup"><span data-stu-id="63eba-116">The type of the second argument of a curried function.</span></span>

## <a name="see-also"></a><span data-ttu-id="63eba-117">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="63eba-117">See Also</span></span>

- [<span data-ttu-id="63eba-118">Microsoft. Quantum. Canon. uncurriedop</span><span class="sxs-lookup"><span data-stu-id="63eba-118">Microsoft.Quantum.Canon.UncurriedOp</span></span>](xref:Microsoft.Quantum.Canon.UncurriedOp)