---
uid: Microsoft.Quantum.Math.PlusA
title: Plusa-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: PlusA
qsharp.summary: Returns the sum (concatenation) of two inputs.
ms.openlocfilehash: 14e9bfdbe4b70b4730e5bfc64a0ee81ab3cecaaf
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842716"
---
# <a name="plusa-function"></a><span data-ttu-id="26296-102">Plusa-Funktion</span><span class="sxs-lookup"><span data-stu-id="26296-102">PlusA function</span></span>

<span data-ttu-id="26296-103">Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="26296-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="26296-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="26296-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="26296-105">Gibt die Summe (Verkettung) von zwei Eingaben zurück.</span><span class="sxs-lookup"><span data-stu-id="26296-105">Returns the sum (concatenation) of two inputs.</span></span>

```qsharp
function PlusA<'Element> (a : 'Element[], b : 'Element[]) : 'Element[]
```


## <a name="input"></a><span data-ttu-id="26296-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="26296-106">Input</span></span>

### <a name="a--element"></a><span data-ttu-id="26296-107">a: ' Element []</span><span class="sxs-lookup"><span data-stu-id="26296-107">a : 'Element[]</span></span>

<span data-ttu-id="26296-108">Die erste Eingabe $a $ summiert.</span><span class="sxs-lookup"><span data-stu-id="26296-108">The first input $a$ to be summed.</span></span>


### <a name="b--element"></a><span data-ttu-id="26296-109">b: ' Element []</span><span class="sxs-lookup"><span data-stu-id="26296-109">b : 'Element[]</span></span>

<span data-ttu-id="26296-110">Die zweite Eingabe $b $ summiert.</span><span class="sxs-lookup"><span data-stu-id="26296-110">The second input $b$ to be summed.</span></span>



## <a name="output--element"></a><span data-ttu-id="26296-111">Ausgabe: ' Element []</span><span class="sxs-lookup"><span data-stu-id="26296-111">Output : 'Element[]</span></span>

<span data-ttu-id="26296-112">Die Summe $a + b $.</span><span class="sxs-lookup"><span data-stu-id="26296-112">The sum $a + b$.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="26296-113">Typparameter</span><span class="sxs-lookup"><span data-stu-id="26296-113">Type Parameters</span></span>

### <a name="element"></a><span data-ttu-id="26296-114">'-Element</span><span class="sxs-lookup"><span data-stu-id="26296-114">'Element</span></span>

<span data-ttu-id="26296-115">Der Typ der einzelnen Elemente in jedem der beiden Eingabe Arrays.</span><span class="sxs-lookup"><span data-stu-id="26296-115">The type of each element in each of the two input arrays.</span></span>