---
uid: Microsoft.Quantum.Canon.Compose
title: Compose-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Compose
qsharp.summary: Returns the composition of two functions.
ms.openlocfilehash: 02cff7eef4d55d27d5d72e6219a90b7d8f5beb3b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704354"
---
# <a name="compose-function"></a><span data-ttu-id="fc393-102">Compose-Funktion</span><span class="sxs-lookup"><span data-stu-id="fc393-102">Compose function</span></span>

<span data-ttu-id="fc393-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="fc393-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="fc393-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="fc393-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="fc393-105">Gibt die Komposition zweier Funktionen zurück.</span><span class="sxs-lookup"><span data-stu-id="fc393-105">Returns the composition of two functions.</span></span>

```qsharp
function Compose<'T, 'U, 'V> (outer : ('U -> 'V), inner : ('T -> 'U)) : ('T -> 'V)
```


## <a name="description"></a><span data-ttu-id="fc393-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fc393-106">Description</span></span>

<span data-ttu-id="fc393-107">Wenn zwei Funktionen $f $ und $g $, gibt eine neue Funktion zurück, die $f \circ g $ darstellt.</span><span class="sxs-lookup"><span data-stu-id="fc393-107">Given two functions $f$ and $g$, returns a new function representing $f \circ g$.</span></span>

## <a name="input"></a><span data-ttu-id="fc393-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="fc393-108">Input</span></span>

### <a name="outer--u---v"></a><span data-ttu-id="fc393-109">Outer: "U->" V</span><span class="sxs-lookup"><span data-stu-id="fc393-109">outer : 'U -> 'V</span></span>

<span data-ttu-id="fc393-110">Die zweite Funktion, die angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="fc393-110">The second function to be applied.</span></span>


### <a name="inner--t---u"></a><span data-ttu-id="fc393-111">innere: 't-> ' U</span><span class="sxs-lookup"><span data-stu-id="fc393-111">inner : 'T -> 'U</span></span>

<span data-ttu-id="fc393-112">Die erste Funktion, die angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="fc393-112">The first function to be applied.</span></span>



## <a name="output--t---v"></a><span data-ttu-id="fc393-113">Ausgabe: 't-> ' V</span><span class="sxs-lookup"><span data-stu-id="fc393-113">Output : 'T -> 'V</span></span>

<span data-ttu-id="fc393-114">Eine neue Funktion $h $, sodass für alle Eingaben $x $, $f (g (x)) = h (x) $.</span><span class="sxs-lookup"><span data-stu-id="fc393-114">A new function $h$ such that for all inputs $x$, $f(g(x)) = h(x)$.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="fc393-115">Typparameter</span><span class="sxs-lookup"><span data-stu-id="fc393-115">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="fc393-116">GIF</span><span class="sxs-lookup"><span data-stu-id="fc393-116">'T</span></span>

<span data-ttu-id="fc393-117">Der Eingabetyp der ersten Funktion, die angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="fc393-117">The input type of the first function to be applied.</span></span>
### <a name="u"></a><span data-ttu-id="fc393-118">"U</span><span class="sxs-lookup"><span data-stu-id="fc393-118">'U</span></span>

<span data-ttu-id="fc393-119">Der Ausgabetyp der ersten Funktion, die angewendet werden soll, und der Eingabetyp der zweiten Funktion, die angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="fc393-119">The output type of the first function to be applied and the input type of the second function to be applied.</span></span>
### <a name="v"></a><span data-ttu-id="fc393-120">"V</span><span class="sxs-lookup"><span data-stu-id="fc393-120">'V</span></span>

<span data-ttu-id="fc393-121">Der Ausgabetyp der zweiten Funktion, die angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="fc393-121">The output type of the second function to be applied.</span></span>