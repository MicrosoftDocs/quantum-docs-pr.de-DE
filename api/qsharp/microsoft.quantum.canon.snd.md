---
uid: Microsoft.Quantum.Canon.Snd
title: Snd-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Snd
qsharp.summary: Given a pair, returns its second element.
ms.openlocfilehash: c05053b45d24c3398526d1269b90bb40d1e0ef27
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703817"
---
# <a name="snd-function"></a><span data-ttu-id="36d07-102">Snd-Funktion</span><span class="sxs-lookup"><span data-stu-id="36d07-102">Snd function</span></span>

<span data-ttu-id="36d07-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="36d07-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="36d07-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="36d07-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="36d07-105">Gibt bei einem Paar das zweite Element zurück.</span><span class="sxs-lookup"><span data-stu-id="36d07-105">Given a pair, returns its second element.</span></span>

```qsharp
function Snd<'T, 'U> (pair : ('T, 'U)) : 'U
```


## <a name="input"></a><span data-ttu-id="36d07-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="36d07-106">Input</span></span>

### <a name="pair--tu"></a><span data-ttu-id="36d07-107">paar: ('t, ' U)</span><span class="sxs-lookup"><span data-stu-id="36d07-107">pair : ('T,'U)</span></span>

<span data-ttu-id="36d07-108">Ein Tupel mit zwei Elementen.</span><span class="sxs-lookup"><span data-stu-id="36d07-108">A tuple with two elements.</span></span>



## <a name="output--u"></a><span data-ttu-id="36d07-109">Ausgabe: "U</span><span class="sxs-lookup"><span data-stu-id="36d07-109">Output : 'U</span></span>

<span data-ttu-id="36d07-110">Das zweite Element von `pair` .</span><span class="sxs-lookup"><span data-stu-id="36d07-110">The second element of `pair`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="36d07-111">Typparameter</span><span class="sxs-lookup"><span data-stu-id="36d07-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="36d07-112">GIF</span><span class="sxs-lookup"><span data-stu-id="36d07-112">'T</span></span>

<span data-ttu-id="36d07-113">Der Typ des ersten Members des Paars.</span><span class="sxs-lookup"><span data-stu-id="36d07-113">The type of the pair's first member.</span></span>
### <a name="u"></a><span data-ttu-id="36d07-114">"U</span><span class="sxs-lookup"><span data-stu-id="36d07-114">'U</span></span>

<span data-ttu-id="36d07-115">Der Typ des zweiten Members des Paars.</span><span class="sxs-lookup"><span data-stu-id="36d07-115">The type of the pair's second member.</span></span>