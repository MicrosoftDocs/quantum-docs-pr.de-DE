---
uid: Microsoft.Quantum.Canon.Compose
title: Compose-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Compose
qsharp.summary: Returns the composition of two functions.
ms.openlocfilehash: 73eab66e2e9a9af56d01db927eb7af38bb56a23e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840910"
---
# <a name="compose-function"></a><span data-ttu-id="fe03d-102">Compose-Funktion</span><span class="sxs-lookup"><span data-stu-id="fe03d-102">Compose function</span></span>

<span data-ttu-id="fe03d-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="fe03d-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="fe03d-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="fe03d-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="fe03d-105">Gibt die Komposition zweier Funktionen zurück.</span><span class="sxs-lookup"><span data-stu-id="fe03d-105">Returns the composition of two functions.</span></span>

```qsharp
function Compose<'T, 'U, 'V> (outer : ('U -> 'V), inner : ('T -> 'U)) : ('T -> 'V)
```


## <a name="description"></a><span data-ttu-id="fe03d-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fe03d-106">Description</span></span>

<span data-ttu-id="fe03d-107">Wenn zwei Funktionen $f $ und $g $, gibt eine neue Funktion zurück, die $f \circ g $ darstellt.</span><span class="sxs-lookup"><span data-stu-id="fe03d-107">Given two functions $f$ and $g$, returns a new function representing $f \circ g$.</span></span>

## <a name="input"></a><span data-ttu-id="fe03d-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="fe03d-108">Input</span></span>

### <a name="outer--u---v"></a><span data-ttu-id="fe03d-109">Outer: "U->" V</span><span class="sxs-lookup"><span data-stu-id="fe03d-109">outer : 'U -> 'V</span></span>

<span data-ttu-id="fe03d-110">Die zweite Funktion, die angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="fe03d-110">The second function to be applied.</span></span>


### <a name="inner--t---u"></a><span data-ttu-id="fe03d-111">innere: 't-> ' U</span><span class="sxs-lookup"><span data-stu-id="fe03d-111">inner : 'T -> 'U</span></span>

<span data-ttu-id="fe03d-112">Die erste Funktion, die angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="fe03d-112">The first function to be applied.</span></span>



## <a name="output--t---v"></a><span data-ttu-id="fe03d-113">Ausgabe: 't-> ' V</span><span class="sxs-lookup"><span data-stu-id="fe03d-113">Output : 'T -> 'V</span></span>

<span data-ttu-id="fe03d-114">Eine neue Funktion $h $, sodass für alle Eingaben $x $, $f (g (x)) = h (x) $.</span><span class="sxs-lookup"><span data-stu-id="fe03d-114">A new function $h$ such that for all inputs $x$, $f(g(x)) = h(x)$.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="fe03d-115">Typparameter</span><span class="sxs-lookup"><span data-stu-id="fe03d-115">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="fe03d-116">GIF</span><span class="sxs-lookup"><span data-stu-id="fe03d-116">'T</span></span>

<span data-ttu-id="fe03d-117">Der Eingabetyp der ersten Funktion, die angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="fe03d-117">The input type of the first function to be applied.</span></span>
### <a name="u"></a><span data-ttu-id="fe03d-118">"U</span><span class="sxs-lookup"><span data-stu-id="fe03d-118">'U</span></span>

<span data-ttu-id="fe03d-119">Der Ausgabetyp der ersten Funktion, die angewendet werden soll, und der Eingabetyp der zweiten Funktion, die angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="fe03d-119">The output type of the first function to be applied and the input type of the second function to be applied.</span></span>
### <a name="v"></a><span data-ttu-id="fe03d-120">"V</span><span class="sxs-lookup"><span data-stu-id="fe03d-120">'V</span></span>

<span data-ttu-id="fe03d-121">Der Ausgabetyp der zweiten Funktion, die angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="fe03d-121">The output type of the second function to be applied.</span></span>