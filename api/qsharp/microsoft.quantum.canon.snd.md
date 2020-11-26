---
uid: Microsoft.Quantum.Canon.Snd
title: Snd-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Snd
qsharp.summary: Given a pair, returns its second element.
ms.openlocfilehash: c935a2bc9e3f5ab32669feae2bfc0f2ebf57e744
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96205319"
---
# <a name="snd-function"></a><span data-ttu-id="22e1e-102">Snd-Funktion</span><span class="sxs-lookup"><span data-stu-id="22e1e-102">Snd function</span></span>

<span data-ttu-id="22e1e-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="22e1e-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="22e1e-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="22e1e-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="22e1e-105">Gibt bei einem Paar das zweite Element zurück.</span><span class="sxs-lookup"><span data-stu-id="22e1e-105">Given a pair, returns its second element.</span></span>

```qsharp
function Snd<'T, 'U> (pair : ('T, 'U)) : 'U
```


## <a name="input"></a><span data-ttu-id="22e1e-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="22e1e-106">Input</span></span>

### <a name="pair--tu"></a><span data-ttu-id="22e1e-107">paar: ('t, ' U)</span><span class="sxs-lookup"><span data-stu-id="22e1e-107">pair : ('T,'U)</span></span>

<span data-ttu-id="22e1e-108">Ein Tupel mit zwei Elementen.</span><span class="sxs-lookup"><span data-stu-id="22e1e-108">A tuple with two elements.</span></span>



## <a name="output--u"></a><span data-ttu-id="22e1e-109">Ausgabe: "U</span><span class="sxs-lookup"><span data-stu-id="22e1e-109">Output : 'U</span></span>

<span data-ttu-id="22e1e-110">Das zweite Element von `pair` .</span><span class="sxs-lookup"><span data-stu-id="22e1e-110">The second element of `pair`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="22e1e-111">Typparameter</span><span class="sxs-lookup"><span data-stu-id="22e1e-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="22e1e-112">GIF</span><span class="sxs-lookup"><span data-stu-id="22e1e-112">'T</span></span>

<span data-ttu-id="22e1e-113">Der Typ des ersten Members des Paars.</span><span class="sxs-lookup"><span data-stu-id="22e1e-113">The type of the pair's first member.</span></span>
### <a name="u"></a><span data-ttu-id="22e1e-114">"U</span><span class="sxs-lookup"><span data-stu-id="22e1e-114">'U</span></span>

<span data-ttu-id="22e1e-115">Der Typ des zweiten Members des Paars.</span><span class="sxs-lookup"><span data-stu-id="22e1e-115">The type of the pair's second member.</span></span>