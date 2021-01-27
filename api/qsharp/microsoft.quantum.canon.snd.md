---
uid: Microsoft.Quantum.Canon.Snd
title: Snd-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Snd
qsharp.summary: Given a pair, returns its second element.
ms.openlocfilehash: 11786fa195de12a7f2e4f2edb00ac0bc1071dd5e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98852151"
---
# <a name="snd-function"></a><span data-ttu-id="ae9b5-102">Snd-Funktion</span><span class="sxs-lookup"><span data-stu-id="ae9b5-102">Snd function</span></span>

<span data-ttu-id="ae9b5-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="ae9b5-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="ae9b5-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="ae9b5-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="ae9b5-105">Gibt bei einem Paar das zweite Element zurück.</span><span class="sxs-lookup"><span data-stu-id="ae9b5-105">Given a pair, returns its second element.</span></span>

```qsharp
function Snd<'T, 'U> (pair : ('T, 'U)) : 'U
```


## <a name="input"></a><span data-ttu-id="ae9b5-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ae9b5-106">Input</span></span>

### <a name="pair--tu"></a><span data-ttu-id="ae9b5-107">paar: ('t, ' U)</span><span class="sxs-lookup"><span data-stu-id="ae9b5-107">pair : ('T,'U)</span></span>

<span data-ttu-id="ae9b5-108">Ein Tupel mit zwei Elementen.</span><span class="sxs-lookup"><span data-stu-id="ae9b5-108">A tuple with two elements.</span></span>



## <a name="output--u"></a><span data-ttu-id="ae9b5-109">Ausgabe: "U</span><span class="sxs-lookup"><span data-stu-id="ae9b5-109">Output : 'U</span></span>

<span data-ttu-id="ae9b5-110">Das zweite Element von `pair` .</span><span class="sxs-lookup"><span data-stu-id="ae9b5-110">The second element of `pair`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="ae9b5-111">Typparameter</span><span class="sxs-lookup"><span data-stu-id="ae9b5-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="ae9b5-112">GIF</span><span class="sxs-lookup"><span data-stu-id="ae9b5-112">'T</span></span>

<span data-ttu-id="ae9b5-113">Der Typ des ersten Members des Paars.</span><span class="sxs-lookup"><span data-stu-id="ae9b5-113">The type of the pair's first member.</span></span>
### <a name="u"></a><span data-ttu-id="ae9b5-114">"U</span><span class="sxs-lookup"><span data-stu-id="ae9b5-114">'U</span></span>

<span data-ttu-id="ae9b5-115">Der Typ des zweiten Members des Paars.</span><span class="sxs-lookup"><span data-stu-id="ae9b5-115">The type of the pair's second member.</span></span>