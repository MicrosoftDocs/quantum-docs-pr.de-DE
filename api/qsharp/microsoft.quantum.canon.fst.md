---
uid: Microsoft.Quantum.Canon.Fst
title: FST-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Fst
qsharp.summary: Given a pair, returns its first element.
ms.openlocfilehash: cd5746358c8323f8d2dbca44965fa5dbac0a84c1
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840518"
---
# <a name="fst-function"></a><span data-ttu-id="133b8-102">FST-Funktion</span><span class="sxs-lookup"><span data-stu-id="133b8-102">Fst function</span></span>

<span data-ttu-id="133b8-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="133b8-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="133b8-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="133b8-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="133b8-105">Gibt bei einem Paar das erste Element zurück.</span><span class="sxs-lookup"><span data-stu-id="133b8-105">Given a pair, returns its first element.</span></span>

```qsharp
function Fst<'T, 'U> (pair : ('T, 'U)) : 'T
```


## <a name="input"></a><span data-ttu-id="133b8-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="133b8-106">Input</span></span>

### <a name="pair--tu"></a><span data-ttu-id="133b8-107">paar: ('t, ' U)</span><span class="sxs-lookup"><span data-stu-id="133b8-107">pair : ('T,'U)</span></span>

<span data-ttu-id="133b8-108">Ein Tupel mit zwei Elementen.</span><span class="sxs-lookup"><span data-stu-id="133b8-108">A tuple with two elements.</span></span>



## <a name="output--t"></a><span data-ttu-id="133b8-109">Ausgabe: 't</span><span class="sxs-lookup"><span data-stu-id="133b8-109">Output : 'T</span></span>

<span data-ttu-id="133b8-110">Das erste Element von `pair`.</span><span class="sxs-lookup"><span data-stu-id="133b8-110">The first element of `pair`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="133b8-111">Typparameter</span><span class="sxs-lookup"><span data-stu-id="133b8-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="133b8-112">GIF</span><span class="sxs-lookup"><span data-stu-id="133b8-112">'T</span></span>

<span data-ttu-id="133b8-113">Der Typ des ersten Members des Paars.</span><span class="sxs-lookup"><span data-stu-id="133b8-113">The type of the pair's first member.</span></span>
### <a name="u"></a><span data-ttu-id="133b8-114">"U</span><span class="sxs-lookup"><span data-stu-id="133b8-114">'U</span></span>

<span data-ttu-id="133b8-115">Der Typ des zweiten Members des Paars.</span><span class="sxs-lookup"><span data-stu-id="133b8-115">The type of the pair's second member.</span></span>