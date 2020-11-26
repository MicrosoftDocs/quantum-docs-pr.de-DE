---
uid: Microsoft.Quantum.Math.PlusA
title: Plusa-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: PlusA
qsharp.summary: Returns the sum (concatenation) of two inputs.
ms.openlocfilehash: fe19c5d2e075624516376a5d5fa49014acb295ec
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96194830"
---
# <a name="plusa-function"></a><span data-ttu-id="82389-102">Plusa-Funktion</span><span class="sxs-lookup"><span data-stu-id="82389-102">PlusA function</span></span>

<span data-ttu-id="82389-103">Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="82389-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="82389-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="82389-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="82389-105">Gibt die Summe (Verkettung) von zwei Eingaben zurück.</span><span class="sxs-lookup"><span data-stu-id="82389-105">Returns the sum (concatenation) of two inputs.</span></span>

```qsharp
function PlusA<'Element> (a : 'Element[], b : 'Element[]) : 'Element[]
```


## <a name="input"></a><span data-ttu-id="82389-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="82389-106">Input</span></span>

### <a name="a--element"></a><span data-ttu-id="82389-107">a: ' Element []</span><span class="sxs-lookup"><span data-stu-id="82389-107">a : 'Element[]</span></span>

<span data-ttu-id="82389-108">Die erste Eingabe $a $ summiert.</span><span class="sxs-lookup"><span data-stu-id="82389-108">The first input $a$ to be summed.</span></span>


### <a name="b--element"></a><span data-ttu-id="82389-109">b: ' Element []</span><span class="sxs-lookup"><span data-stu-id="82389-109">b : 'Element[]</span></span>

<span data-ttu-id="82389-110">Die zweite Eingabe $b $ summiert.</span><span class="sxs-lookup"><span data-stu-id="82389-110">The second input $b$ to be summed.</span></span>



## <a name="output--element"></a><span data-ttu-id="82389-111">Ausgabe: ' Element []</span><span class="sxs-lookup"><span data-stu-id="82389-111">Output : 'Element[]</span></span>

<span data-ttu-id="82389-112">Die Summe $a + b $.</span><span class="sxs-lookup"><span data-stu-id="82389-112">The sum $a + b$.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="82389-113">Typparameter</span><span class="sxs-lookup"><span data-stu-id="82389-113">Type Parameters</span></span>

### <a name="element"></a><span data-ttu-id="82389-114">'-Element</span><span class="sxs-lookup"><span data-stu-id="82389-114">'Element</span></span>

<span data-ttu-id="82389-115">Der Typ der einzelnen Elemente in jedem der beiden Eingabe Arrays.</span><span class="sxs-lookup"><span data-stu-id="82389-115">The type of each element in each of the two input arrays.</span></span>