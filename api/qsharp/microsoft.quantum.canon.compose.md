---
uid: Microsoft.Quantum.Canon.Compose
title: Compose-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Compose
qsharp.summary: Returns the composition of two functions.
ms.openlocfilehash: f8c6ad36220b48be1723c2d91cbf7c0a4947af14
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96216760"
---
# <a name="compose-function"></a><span data-ttu-id="2cc83-102">Compose-Funktion</span><span class="sxs-lookup"><span data-stu-id="2cc83-102">Compose function</span></span>

<span data-ttu-id="2cc83-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="2cc83-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="2cc83-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="2cc83-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="2cc83-105">Gibt die Komposition zweier Funktionen zurück.</span><span class="sxs-lookup"><span data-stu-id="2cc83-105">Returns the composition of two functions.</span></span>

```qsharp
function Compose<'T, 'U, 'V> (outer : ('U -> 'V), inner : ('T -> 'U)) : ('T -> 'V)
```


## <a name="description"></a><span data-ttu-id="2cc83-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2cc83-106">Description</span></span>

<span data-ttu-id="2cc83-107">Wenn zwei Funktionen $f $ und $g $, gibt eine neue Funktion zurück, die $f \circ g $ darstellt.</span><span class="sxs-lookup"><span data-stu-id="2cc83-107">Given two functions $f$ and $g$, returns a new function representing $f \circ g$.</span></span>

## <a name="input"></a><span data-ttu-id="2cc83-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2cc83-108">Input</span></span>

### <a name="outer--u---v"></a><span data-ttu-id="2cc83-109">Outer: "U->" V</span><span class="sxs-lookup"><span data-stu-id="2cc83-109">outer : 'U -> 'V</span></span>

<span data-ttu-id="2cc83-110">Die zweite Funktion, die angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="2cc83-110">The second function to be applied.</span></span>


### <a name="inner--t---u"></a><span data-ttu-id="2cc83-111">innere: 't-> ' U</span><span class="sxs-lookup"><span data-stu-id="2cc83-111">inner : 'T -> 'U</span></span>

<span data-ttu-id="2cc83-112">Die erste Funktion, die angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="2cc83-112">The first function to be applied.</span></span>



## <a name="output--t---v"></a><span data-ttu-id="2cc83-113">Ausgabe: 't-> ' V</span><span class="sxs-lookup"><span data-stu-id="2cc83-113">Output : 'T -> 'V</span></span>

<span data-ttu-id="2cc83-114">Eine neue Funktion $h $, sodass für alle Eingaben $x $, $f (g (x)) = h (x) $.</span><span class="sxs-lookup"><span data-stu-id="2cc83-114">A new function $h$ such that for all inputs $x$, $f(g(x)) = h(x)$.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="2cc83-115">Typparameter</span><span class="sxs-lookup"><span data-stu-id="2cc83-115">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="2cc83-116">GIF</span><span class="sxs-lookup"><span data-stu-id="2cc83-116">'T</span></span>

<span data-ttu-id="2cc83-117">Der Eingabetyp der ersten Funktion, die angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="2cc83-117">The input type of the first function to be applied.</span></span>
### <a name="u"></a><span data-ttu-id="2cc83-118">"U</span><span class="sxs-lookup"><span data-stu-id="2cc83-118">'U</span></span>

<span data-ttu-id="2cc83-119">Der Ausgabetyp der ersten Funktion, die angewendet werden soll, und der Eingabetyp der zweiten Funktion, die angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="2cc83-119">The output type of the first function to be applied and the input type of the second function to be applied.</span></span>
### <a name="v"></a><span data-ttu-id="2cc83-120">"V</span><span class="sxs-lookup"><span data-stu-id="2cc83-120">'V</span></span>

<span data-ttu-id="2cc83-121">Der Ausgabetyp der zweiten Funktion, die angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="2cc83-121">The output type of the second function to be applied.</span></span>