---
uid: Microsoft.Quantum.Canon.UncurriedOp
title: Uncurriedop-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: UncurriedOp
qsharp.summary: Given a function which returns operations, returns a new operation which takes both inputs as a tuple.
ms.openlocfilehash: 359c0b2a9dd56445fb39fadc6580809dd9fbf628
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703727"
---
# <a name="uncurriedop-function"></a><span data-ttu-id="91c2c-102">Uncurriedop-Funktion</span><span class="sxs-lookup"><span data-stu-id="91c2c-102">UncurriedOp function</span></span>

<span data-ttu-id="91c2c-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="91c2c-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="91c2c-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="91c2c-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="91c2c-105">Gibt eine Funktion zurück, die Vorgänge zurückgibt, gibt einen neuen Vorgang zurück, der beide Eingaben als Tupel annimmt.</span><span class="sxs-lookup"><span data-stu-id="91c2c-105">Given a function which returns operations, returns a new operation which takes both inputs as a tuple.</span></span>

```qsharp
function UncurriedOp<'T, 'U> (curriedOp : ('T -> ('U => Unit))) : (('T, 'U) => Unit)
```


## <a name="input"></a><span data-ttu-id="91c2c-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="91c2c-106">Input</span></span>

### <a name="curriedop--t---u--unit"></a><span data-ttu-id="91c2c-107">curriedop: 't-> ' U => [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="91c2c-107">curriedOp : 'T -> 'U => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="91c2c-108">Eine Funktion, die Vorgänge zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="91c2c-108">A function which returns operations.</span></span>



## <a name="output--tu--unit"></a><span data-ttu-id="91c2c-109">Ausgabe: ('t, ' U) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="91c2c-109">Output : ('T,'U) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="91c2c-110">Ein neuer Vorgang `op` , der `op(t, u)` entspricht `(curriedOp(t))(u)` .</span><span class="sxs-lookup"><span data-stu-id="91c2c-110">A new operation `op` such that `op(t, u)` is equivalent to `(curriedOp(t))(u)`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="91c2c-111">Typparameter</span><span class="sxs-lookup"><span data-stu-id="91c2c-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="91c2c-112">GIF</span><span class="sxs-lookup"><span data-stu-id="91c2c-112">'T</span></span>

<span data-ttu-id="91c2c-113">Der Typ der ersten Eingabe für einen geschweifenden Vorgang.</span><span class="sxs-lookup"><span data-stu-id="91c2c-113">The type of the first input to a curried operation.</span></span>
### <a name="u"></a><span data-ttu-id="91c2c-114">"U</span><span class="sxs-lookup"><span data-stu-id="91c2c-114">'U</span></span>

<span data-ttu-id="91c2c-115">Der Typ der zweiten Eingabe für einen geschweifenden Vorgang.</span><span class="sxs-lookup"><span data-stu-id="91c2c-115">The type of the second input to a curried operation.</span></span>

## <a name="see-also"></a><span data-ttu-id="91c2c-116">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="91c2c-116">See Also</span></span>

- [<span data-ttu-id="91c2c-117">Microsoft. Quantum. Canon. uncurriedopc</span><span class="sxs-lookup"><span data-stu-id="91c2c-117">Microsoft.Quantum.Canon.UncurriedOpC</span></span>](xref:Microsoft.Quantum.Canon.UncurriedOpC)
- [<span data-ttu-id="91c2c-118">Microsoft. Quantum. Canon. uncurriedopa</span><span class="sxs-lookup"><span data-stu-id="91c2c-118">Microsoft.Quantum.Canon.UncurriedOpA</span></span>](xref:Microsoft.Quantum.Canon.UncurriedOpA)
- [<span data-ttu-id="91c2c-119">Microsoft. Quantum. Canon. uncurriedopca</span><span class="sxs-lookup"><span data-stu-id="91c2c-119">Microsoft.Quantum.Canon.UncurriedOpCA</span></span>](xref:Microsoft.Quantum.Canon.UncurriedOpCA)