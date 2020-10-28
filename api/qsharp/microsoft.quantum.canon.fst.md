---
uid: Microsoft.Quantum.Canon.Fst
title: FST-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Fst
qsharp.summary: Given a pair, returns its first element.
ms.openlocfilehash: 88ff5e29de9eeefcc1e207f277c37c63cb0faade
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704178"
---
# <a name="fst-function"></a><span data-ttu-id="fa753-102">FST-Funktion</span><span class="sxs-lookup"><span data-stu-id="fa753-102">Fst function</span></span>

<span data-ttu-id="fa753-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="fa753-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="fa753-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="fa753-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="fa753-105">Gibt bei einem Paar das erste Element zurück.</span><span class="sxs-lookup"><span data-stu-id="fa753-105">Given a pair, returns its first element.</span></span>

```qsharp
function Fst<'T, 'U> (pair : ('T, 'U)) : 'T
```


## <a name="input"></a><span data-ttu-id="fa753-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="fa753-106">Input</span></span>

### <a name="pair--tu"></a><span data-ttu-id="fa753-107">paar: ('t, ' U)</span><span class="sxs-lookup"><span data-stu-id="fa753-107">pair : ('T,'U)</span></span>

<span data-ttu-id="fa753-108">Ein Tupel mit zwei Elementen.</span><span class="sxs-lookup"><span data-stu-id="fa753-108">A tuple with two elements.</span></span>



## <a name="output--t"></a><span data-ttu-id="fa753-109">Ausgabe: 't</span><span class="sxs-lookup"><span data-stu-id="fa753-109">Output : 'T</span></span>

<span data-ttu-id="fa753-110">Das erste Element von `pair`.</span><span class="sxs-lookup"><span data-stu-id="fa753-110">The first element of `pair`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="fa753-111">Typparameter</span><span class="sxs-lookup"><span data-stu-id="fa753-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="fa753-112">GIF</span><span class="sxs-lookup"><span data-stu-id="fa753-112">'T</span></span>

<span data-ttu-id="fa753-113">Der Typ des ersten Members des Paars.</span><span class="sxs-lookup"><span data-stu-id="fa753-113">The type of the pair's first member.</span></span>
### <a name="u"></a><span data-ttu-id="fa753-114">"U</span><span class="sxs-lookup"><span data-stu-id="fa753-114">'U</span></span>

<span data-ttu-id="fa753-115">Der Typ des zweiten Members des Paars.</span><span class="sxs-lookup"><span data-stu-id="fa753-115">The type of the pair's second member.</span></span>