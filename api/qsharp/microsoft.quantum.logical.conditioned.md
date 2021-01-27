---
uid: Microsoft.Quantum.Logical.Conditioned
title: Bedingte Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: Conditioned
qsharp.summary: Returns one of two values, depending on the value of a Boolean condition.
ms.openlocfilehash: ea3b8eba960acceb6540978c6fccd9f796b0f67d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98817287"
---
# <a name="conditioned-function"></a><span data-ttu-id="d79b9-102">Bedingte Funktion</span><span class="sxs-lookup"><span data-stu-id="d79b9-102">Conditioned function</span></span>

<span data-ttu-id="d79b9-103">Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="d79b9-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="d79b9-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="d79b9-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="d79b9-105">Gibt je nach dem Wert einer booleschen Bedingung einen von zwei Werten zurück.</span><span class="sxs-lookup"><span data-stu-id="d79b9-105">Returns one of two values, depending on the value of a Boolean condition.</span></span>

```qsharp
function Conditioned<'T> (condition : Bool, ifTrue : 'T, ifFalse : 'T) : 'T
```


## <a name="input"></a><span data-ttu-id="d79b9-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d79b9-106">Input</span></span>

### <a name="condition--bool"></a><span data-ttu-id="d79b9-107">Bedingung: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="d79b9-107">condition : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="d79b9-108">Eine Bedingung, mit der gesteuert wird, welche Eingaben zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="d79b9-108">A condition used to control which input is returned.</span></span>


### <a name="iftrue--t"></a><span data-ttu-id="d79b9-109">IfTrue: 't</span><span class="sxs-lookup"><span data-stu-id="d79b9-109">ifTrue : 'T</span></span>

<span data-ttu-id="d79b9-110">Der Wert, der zurückgegeben werden soll, wenn `condition` ist `true` .</span><span class="sxs-lookup"><span data-stu-id="d79b9-110">The value to be returned when `condition` is `true`.</span></span>


### <a name="iffalse--t"></a><span data-ttu-id="d79b9-111">IfFalse: 't</span><span class="sxs-lookup"><span data-stu-id="d79b9-111">ifFalse : 'T</span></span>

<span data-ttu-id="d79b9-112">Der Wert, der zurückgegeben werden soll, wenn `condition` ist `false` .</span><span class="sxs-lookup"><span data-stu-id="d79b9-112">The value to be returned when `condition` is `false`.</span></span>



## <a name="output--t"></a><span data-ttu-id="d79b9-113">Ausgabe: 't</span><span class="sxs-lookup"><span data-stu-id="d79b9-113">Output : 'T</span></span>

<span data-ttu-id="d79b9-114">`ifTrue` , wenn den Wert `condition` `true` hat und `ifFalse` andernfalls.</span><span class="sxs-lookup"><span data-stu-id="d79b9-114">`ifTrue` if `condition` is `true`, and `ifFalse` otherwise.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="d79b9-115">Typparameter</span><span class="sxs-lookup"><span data-stu-id="d79b9-115">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="d79b9-116">GIF</span><span class="sxs-lookup"><span data-stu-id="d79b9-116">'T</span></span>



## <a name="remarks"></a><span data-ttu-id="d79b9-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d79b9-117">Remarks</span></span>

<span data-ttu-id="d79b9-118">Im Gegensatz zum- `?|` Operator ist diese Funktion nicht kurz, sodass beide Eingaben vollständig ausgewertet werden.</span><span class="sxs-lookup"><span data-stu-id="d79b9-118">Unlike the `?|` operator, this function does not short-circuit, such that both inputs are fully evaluated.</span></span>

<span data-ttu-id="d79b9-119">Bis zu einem kurzen Schluss Verhalten sind die folgenden äquivalent:</span><span class="sxs-lookup"><span data-stu-id="d79b9-119">Up to short-circuiting behavior, the following are equivalent:</span></span>

```qsharp
let x = condition ? ifTrue | ifFalse;
let x = Conditioned(condition, ifTrue, ifFalse);
```