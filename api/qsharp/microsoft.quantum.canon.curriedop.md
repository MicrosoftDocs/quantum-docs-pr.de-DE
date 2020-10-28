---
uid: Microsoft.Quantum.Canon.CurriedOp
title: Curriedop-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: CurriedOp
qsharp.summary: >-
  Returns a curried version of an operation on two inputs.

  That is, given an operation with two inputs, this function applies Curry's isomorphism $f(x, y) \equiv f(x)(y)$ to return an operation of one input which returns an operation of one input.
ms.openlocfilehash: 13bc3e195d8a4ba26b726f96e4dc6b83da43c3e7
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704282"
---
# <a name="curriedop-function"></a><span data-ttu-id="edd1e-102">Curriedop-Funktion</span><span class="sxs-lookup"><span data-stu-id="edd1e-102">CurriedOp function</span></span>

<span data-ttu-id="edd1e-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="edd1e-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="edd1e-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="edd1e-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="edd1e-105">Gibt eine Curry-Version eines Vorgangs für zwei Eingaben zurück.</span><span class="sxs-lookup"><span data-stu-id="edd1e-105">Returns a curried version of an operation on two inputs.</span></span>

<span data-ttu-id="edd1e-106">Bei einem Vorgang mit zwei Eingaben wendet diese Funktion z. b. die "isomorphism"-$f (x, y) \equiv f (x) (y) $ an, um einen Vorgang mit einer Eingabe zurückzugeben, der einen Vorgang mit einer Eingabe zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="edd1e-106">That is, given an operation with two inputs, this function applies Curry's isomorphism $f(x, y) \equiv f(x)(y)$ to return an operation of one input which returns an operation of one input.</span></span>

```qsharp
function CurriedOp<'T, 'U> (op : (('T, 'U) => Unit)) : ('T -> ('U => Unit))
```


## <a name="input"></a><span data-ttu-id="edd1e-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="edd1e-107">Input</span></span>

### <a name="op--tu--unit"></a><span data-ttu-id="edd1e-108">OP: ('t, ' U) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="edd1e-108">op : ('T,'U) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="edd1e-109">Ein Vorgang, dessen Eingabe ein paar ist.</span><span class="sxs-lookup"><span data-stu-id="edd1e-109">An operation whose input is a pair.</span></span>



## <a name="output--t---u--unit"></a><span data-ttu-id="edd1e-110">Ausgabe: 't-> ' U => [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="edd1e-110">Output : 'T -> 'U => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="edd1e-111">Ein Vorgang, der das erste Element eines Paars akzeptiert und einen Vorgang zurückgibt, der als Eingabe das zweite Element der ursprünglichen Vorgangs Eingabe akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="edd1e-111">An operation which accepts the first element of a pair and returns an operation which accepts as its input the second element of the original operation's input.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="edd1e-112">Typparameter</span><span class="sxs-lookup"><span data-stu-id="edd1e-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="edd1e-113">GIF</span><span class="sxs-lookup"><span data-stu-id="edd1e-113">'T</span></span>

<span data-ttu-id="edd1e-114">Der Typ der ersten Komponente einer Funktion, die für Paare definiert ist.</span><span class="sxs-lookup"><span data-stu-id="edd1e-114">The type of the first component of a function defined on pairs.</span></span>
### <a name="u"></a><span data-ttu-id="edd1e-115">"U</span><span class="sxs-lookup"><span data-stu-id="edd1e-115">'U</span></span>

<span data-ttu-id="edd1e-116">Der Typ der zweiten Komponente einer Funktion, die für Paare definiert ist.</span><span class="sxs-lookup"><span data-stu-id="edd1e-116">The type of the second component of a function defined on pairs.</span></span>

## <a name="remarks"></a><span data-ttu-id="edd1e-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="edd1e-117">Remarks</span></span>

<span data-ttu-id="edd1e-118">Die folgenden sind gleichwertig:</span><span class="sxs-lookup"><span data-stu-id="edd1e-118">The following are equivalent:</span></span>

```qsharp
op(x, y);

let curried = CurriedOp(op);
let partial = curried(x);
partial(y);
```