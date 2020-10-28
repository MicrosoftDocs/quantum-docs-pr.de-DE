---
uid: Microsoft.Quantum.Math.PlusA
title: Plusa-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: PlusA
qsharp.summary: Returns the sum (concatenation) of two inputs.
ms.openlocfilehash: 0c6fdcf7c59dc5d89bf83e285339046b5ad5a57e
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92701310"
---
# <a name="plusa-function"></a><span data-ttu-id="079da-102">Plusa-Funktion</span><span class="sxs-lookup"><span data-stu-id="079da-102">PlusA function</span></span>

<span data-ttu-id="079da-103">Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="079da-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="079da-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="079da-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="079da-105">Gibt die Summe (Verkettung) von zwei Eingaben zurück.</span><span class="sxs-lookup"><span data-stu-id="079da-105">Returns the sum (concatenation) of two inputs.</span></span>

```qsharp
function PlusA<'Element> (a : 'Element[], b : 'Element[]) : 'Element[]
```


## <a name="input"></a><span data-ttu-id="079da-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="079da-106">Input</span></span>

### <a name="a--element"></a><span data-ttu-id="079da-107">a: ' Element []</span><span class="sxs-lookup"><span data-stu-id="079da-107">a : 'Element[]</span></span>

<span data-ttu-id="079da-108">Die erste Eingabe $a $ summiert.</span><span class="sxs-lookup"><span data-stu-id="079da-108">The first input $a$ to be summed.</span></span>


### <a name="b--element"></a><span data-ttu-id="079da-109">b: ' Element []</span><span class="sxs-lookup"><span data-stu-id="079da-109">b : 'Element[]</span></span>

<span data-ttu-id="079da-110">Die zweite Eingabe $b $ summiert.</span><span class="sxs-lookup"><span data-stu-id="079da-110">The second input $b$ to be summed.</span></span>



## <a name="output--element"></a><span data-ttu-id="079da-111">Ausgabe: ' Element []</span><span class="sxs-lookup"><span data-stu-id="079da-111">Output : 'Element[]</span></span>

<span data-ttu-id="079da-112">Die Summe $a + b $.</span><span class="sxs-lookup"><span data-stu-id="079da-112">The sum $a + b$.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="079da-113">Typparameter</span><span class="sxs-lookup"><span data-stu-id="079da-113">Type Parameters</span></span>

### <a name="element"></a><span data-ttu-id="079da-114">'-Element</span><span class="sxs-lookup"><span data-stu-id="079da-114">'Element</span></span>

<span data-ttu-id="079da-115">Der Typ der einzelnen Elemente in jedem der beiden Eingabe Arrays.</span><span class="sxs-lookup"><span data-stu-id="079da-115">The type of each element in each of the two input arrays.</span></span>