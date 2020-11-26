---
uid: Microsoft.Quantum.Canon.Fst
title: FST-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Fst
qsharp.summary: Given a pair, returns its first element.
ms.openlocfilehash: 634f11881a054df7fe79d889832ea6bd80a7394f
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96206934"
---
# <a name="fst-function"></a><span data-ttu-id="4e13b-102">FST-Funktion</span><span class="sxs-lookup"><span data-stu-id="4e13b-102">Fst function</span></span>

<span data-ttu-id="4e13b-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="4e13b-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="4e13b-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="4e13b-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="4e13b-105">Gibt bei einem Paar das erste Element zurück.</span><span class="sxs-lookup"><span data-stu-id="4e13b-105">Given a pair, returns its first element.</span></span>

```qsharp
function Fst<'T, 'U> (pair : ('T, 'U)) : 'T
```


## <a name="input"></a><span data-ttu-id="4e13b-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="4e13b-106">Input</span></span>

### <a name="pair--tu"></a><span data-ttu-id="4e13b-107">paar: ('t, ' U)</span><span class="sxs-lookup"><span data-stu-id="4e13b-107">pair : ('T,'U)</span></span>

<span data-ttu-id="4e13b-108">Ein Tupel mit zwei Elementen.</span><span class="sxs-lookup"><span data-stu-id="4e13b-108">A tuple with two elements.</span></span>



## <a name="output--t"></a><span data-ttu-id="4e13b-109">Ausgabe: 't</span><span class="sxs-lookup"><span data-stu-id="4e13b-109">Output : 'T</span></span>

<span data-ttu-id="4e13b-110">Das erste Element von `pair`.</span><span class="sxs-lookup"><span data-stu-id="4e13b-110">The first element of `pair`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="4e13b-111">Typparameter</span><span class="sxs-lookup"><span data-stu-id="4e13b-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="4e13b-112">GIF</span><span class="sxs-lookup"><span data-stu-id="4e13b-112">'T</span></span>

<span data-ttu-id="4e13b-113">Der Typ des ersten Members des Paars.</span><span class="sxs-lookup"><span data-stu-id="4e13b-113">The type of the pair's first member.</span></span>
### <a name="u"></a><span data-ttu-id="4e13b-114">"U</span><span class="sxs-lookup"><span data-stu-id="4e13b-114">'U</span></span>

<span data-ttu-id="4e13b-115">Der Typ des zweiten Members des Paars.</span><span class="sxs-lookup"><span data-stu-id="4e13b-115">The type of the pair's second member.</span></span>