---
uid: Microsoft.Quantum.Canon.UncurriedOpA
title: Uncurriedopa-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: UncurriedOpA
qsharp.summary: Given a function which returns operations, returns a new operation which takes both inputs as a tuple. The modifier `A` indicates that the operations are adjointable.
ms.openlocfilehash: feb5da771ee6cb6a750fa76f9ffd8f5a3e0b5734
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840052"
---
# <a name="uncurriedopa-function"></a><span data-ttu-id="64f9d-102">Uncurriedopa-Funktion</span><span class="sxs-lookup"><span data-stu-id="64f9d-102">UncurriedOpA function</span></span>

<span data-ttu-id="64f9d-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="64f9d-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="64f9d-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="64f9d-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="64f9d-105">Gibt eine Funktion zurück, die Vorgänge zurückgibt, gibt einen neuen Vorgang zurück, der beide Eingaben als Tupel annimmt.</span><span class="sxs-lookup"><span data-stu-id="64f9d-105">Given a function which returns operations, returns a new operation which takes both inputs as a tuple.</span></span>
<span data-ttu-id="64f9d-106">Der-Modifizierer `A` gibt an, dass die Vorgänge adjointable sind.</span><span class="sxs-lookup"><span data-stu-id="64f9d-106">The modifier `A` indicates that the operations are adjointable.</span></span>

```qsharp
function UncurriedOpA<'T, 'U> (curriedOp : ('T -> ('U => Unit is Adj))) : (('T, 'U) => Unit is Adj)
```


## <a name="input"></a><span data-ttu-id="64f9d-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="64f9d-107">Input</span></span>

### <a name="curriedop--t---u--unit--is-adj"></a><span data-ttu-id="64f9d-108">curriedop: 't-> ' U => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ</span><span class="sxs-lookup"><span data-stu-id="64f9d-108">curriedOp : 'T -> 'U => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="64f9d-109">Eine Funktion, die Vorgänge zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="64f9d-109">A function which returns operations.</span></span>



## <a name="output--tu--unit--is-adj"></a><span data-ttu-id="64f9d-110">Ausgabe: ('t, ' U) => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ</span><span class="sxs-lookup"><span data-stu-id="64f9d-110">Output : ('T,'U) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="64f9d-111">Ein neuer Vorgang `op` , der `op(t, u)` entspricht `(curriedOp(t))(u)` .</span><span class="sxs-lookup"><span data-stu-id="64f9d-111">A new operation `op` such that `op(t, u)` is equivalent to `(curriedOp(t))(u)`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="64f9d-112">Typparameter</span><span class="sxs-lookup"><span data-stu-id="64f9d-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="64f9d-113">GIF</span><span class="sxs-lookup"><span data-stu-id="64f9d-113">'T</span></span>

<span data-ttu-id="64f9d-114">Der Typ des ersten Arguments einer Curry-Funktion.</span><span class="sxs-lookup"><span data-stu-id="64f9d-114">The type of the first argument of a curried function.</span></span>
### <a name="u"></a><span data-ttu-id="64f9d-115">"U</span><span class="sxs-lookup"><span data-stu-id="64f9d-115">'U</span></span>

<span data-ttu-id="64f9d-116">Der Typ des zweiten Arguments einer Curry-Funktion.</span><span class="sxs-lookup"><span data-stu-id="64f9d-116">The type of the second argument of a curried function.</span></span>

## <a name="see-also"></a><span data-ttu-id="64f9d-117">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="64f9d-117">See Also</span></span>

- [<span data-ttu-id="64f9d-118">Microsoft. Quantum. Canon. uncurriedop</span><span class="sxs-lookup"><span data-stu-id="64f9d-118">Microsoft.Quantum.Canon.UncurriedOp</span></span>](xref:Microsoft.Quantum.Canon.UncurriedOp)