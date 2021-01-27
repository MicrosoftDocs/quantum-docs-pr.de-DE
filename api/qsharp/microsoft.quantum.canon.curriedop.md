---
uid: Microsoft.Quantum.Canon.CurriedOp
title: Curriedop-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: CurriedOp
qsharp.summary: >-
  Returns a curried version of an operation on two inputs.

  That is, given an operation with two inputs, this function applies Curry's isomorphism $f(x, y) \equiv f(x)(y)$ to return an operation of one input which returns an operation of one input.
ms.openlocfilehash: f811347d65a6460690163e9df631979c906bd89f
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840770"
---
# <a name="curriedop-function"></a><span data-ttu-id="75b58-102">Curriedop-Funktion</span><span class="sxs-lookup"><span data-stu-id="75b58-102">CurriedOp function</span></span>

<span data-ttu-id="75b58-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="75b58-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="75b58-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="75b58-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="75b58-105">Gibt eine Curry-Version eines Vorgangs für zwei Eingaben zurück.</span><span class="sxs-lookup"><span data-stu-id="75b58-105">Returns a curried version of an operation on two inputs.</span></span>

<span data-ttu-id="75b58-106">Bei einem Vorgang mit zwei Eingaben wendet diese Funktion z. b. die "isomorphism"-$f (x, y) \equiv f (x) (y) $ an, um einen Vorgang mit einer Eingabe zurückzugeben, der einen Vorgang mit einer Eingabe zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="75b58-106">That is, given an operation with two inputs, this function applies Curry's isomorphism $f(x, y) \equiv f(x)(y)$ to return an operation of one input which returns an operation of one input.</span></span>

```qsharp
function CurriedOp<'T, 'U> (op : (('T, 'U) => Unit)) : ('T -> ('U => Unit))
```


## <a name="input"></a><span data-ttu-id="75b58-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="75b58-107">Input</span></span>

### <a name="op--tu--unit"></a><span data-ttu-id="75b58-108">OP: ('t, ' U) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="75b58-108">op : ('T,'U) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="75b58-109">Ein Vorgang, dessen Eingabe ein paar ist.</span><span class="sxs-lookup"><span data-stu-id="75b58-109">An operation whose input is a pair.</span></span>



## <a name="output--t---u--unit"></a><span data-ttu-id="75b58-110">Ausgabe: 't-> ' U => [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="75b58-110">Output : 'T -> 'U => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="75b58-111">Ein Vorgang, der das erste Element eines Paars akzeptiert und einen Vorgang zurückgibt, der als Eingabe das zweite Element der ursprünglichen Vorgangs Eingabe akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="75b58-111">An operation which accepts the first element of a pair and returns an operation which accepts as its input the second element of the original operation's input.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="75b58-112">Typparameter</span><span class="sxs-lookup"><span data-stu-id="75b58-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="75b58-113">GIF</span><span class="sxs-lookup"><span data-stu-id="75b58-113">'T</span></span>

<span data-ttu-id="75b58-114">Der Typ der ersten Komponente einer Funktion, die für Paare definiert ist.</span><span class="sxs-lookup"><span data-stu-id="75b58-114">The type of the first component of a function defined on pairs.</span></span>
### <a name="u"></a><span data-ttu-id="75b58-115">"U</span><span class="sxs-lookup"><span data-stu-id="75b58-115">'U</span></span>

<span data-ttu-id="75b58-116">Der Typ der zweiten Komponente einer Funktion, die für Paare definiert ist.</span><span class="sxs-lookup"><span data-stu-id="75b58-116">The type of the second component of a function defined on pairs.</span></span>

## <a name="remarks"></a><span data-ttu-id="75b58-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="75b58-117">Remarks</span></span>

<span data-ttu-id="75b58-118">Die folgenden sind gleichwertig:</span><span class="sxs-lookup"><span data-stu-id="75b58-118">The following are equivalent:</span></span>

```qsharp
op(x, y);

let curried = CurriedOp(op);
let partial = curried(x);
partial(y);
```