---
uid: Microsoft.Quantum.Canon.UncurriedOpC
title: Uncurriedopc-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: UncurriedOpC
qsharp.summary: Given a function which returns operations, returns a new operation which takes both inputs as a tuple. The modifier `C` indicates that the operations are controllable.
ms.openlocfilehash: 35be5425fcd76eae9e0a6fde6a689a5db00da52f
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96204588"
---
# <a name="uncurriedopc-function"></a><span data-ttu-id="3a5ca-102">Uncurriedopc-Funktion</span><span class="sxs-lookup"><span data-stu-id="3a5ca-102">UncurriedOpC function</span></span>

<span data-ttu-id="3a5ca-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="3a5ca-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="3a5ca-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="3a5ca-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="3a5ca-105">Gibt eine Funktion zurück, die Vorgänge zurückgibt, gibt einen neuen Vorgang zurück, der beide Eingaben als Tupel annimmt.</span><span class="sxs-lookup"><span data-stu-id="3a5ca-105">Given a function which returns operations, returns a new operation which takes both inputs as a tuple.</span></span>
<span data-ttu-id="3a5ca-106">Der-Modifizierer `C` gibt an, dass die Vorgänge steuerbar sind.</span><span class="sxs-lookup"><span data-stu-id="3a5ca-106">The modifier `C` indicates that the operations are controllable.</span></span>

```qsharp
function UncurriedOpC<'T, 'U> (curriedOp : ('T -> ('U => Unit is Ctl))) : (('T, 'U) => Unit is Ctl)
```


## <a name="input"></a><span data-ttu-id="3a5ca-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="3a5ca-107">Input</span></span>

### <a name="curriedop--t---u--unit--is-ctl"></a><span data-ttu-id="3a5ca-108">curriedop: 't-> ' U => [Unit](xref:microsoft.quantum.lang-ref.unit)  ist CTL</span><span class="sxs-lookup"><span data-stu-id="3a5ca-108">curriedOp : 'T -> 'U => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="3a5ca-109">Eine Funktion, die Vorgänge zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="3a5ca-109">A function which returns operations.</span></span>



## <a name="output--tu--unit--is-ctl"></a><span data-ttu-id="3a5ca-110">Ausgabe: ('t, ' U) => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist CTL</span><span class="sxs-lookup"><span data-stu-id="3a5ca-110">Output : ('T,'U) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="3a5ca-111">Ein neuer Vorgang `op` , der `op(t, u)` entspricht `(curriedOp(t))(u)` .</span><span class="sxs-lookup"><span data-stu-id="3a5ca-111">A new operation `op` such that `op(t, u)` is equivalent to `(curriedOp(t))(u)`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="3a5ca-112">Typparameter</span><span class="sxs-lookup"><span data-stu-id="3a5ca-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="3a5ca-113">GIF</span><span class="sxs-lookup"><span data-stu-id="3a5ca-113">'T</span></span>

<span data-ttu-id="3a5ca-114">Der Typ des ersten Arguments einer Curry-Funktion.</span><span class="sxs-lookup"><span data-stu-id="3a5ca-114">The type of the first argument of a curried function.</span></span>
### <a name="u"></a><span data-ttu-id="3a5ca-115">"U</span><span class="sxs-lookup"><span data-stu-id="3a5ca-115">'U</span></span>

<span data-ttu-id="3a5ca-116">Der Typ des zweiten Arguments einer Curry-Funktion.</span><span class="sxs-lookup"><span data-stu-id="3a5ca-116">The type of the second argument of a curried function.</span></span>

## <a name="see-also"></a><span data-ttu-id="3a5ca-117">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="3a5ca-117">See Also</span></span>

- [<span data-ttu-id="3a5ca-118">Microsoft. Quantum. Canon. uncurriedop</span><span class="sxs-lookup"><span data-stu-id="3a5ca-118">Microsoft.Quantum.Canon.UncurriedOp</span></span>](xref:Microsoft.Quantum.Canon.UncurriedOp)