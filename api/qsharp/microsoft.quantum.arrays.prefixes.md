---
uid: Microsoft.Quantum.Arrays.Prefixes
title: Präfixe-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Prefixes
qsharp.summary: Given an array, returns all its prefixes.
ms.openlocfilehash: 3501c11437534b1623bffba272a4517487e5634a
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220387"
---
# <a name="prefixes-function"></a><span data-ttu-id="c8307-102">Präfixe-Funktion</span><span class="sxs-lookup"><span data-stu-id="c8307-102">Prefixes function</span></span>

<span data-ttu-id="c8307-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="c8307-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="c8307-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="c8307-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="c8307-105">Gibt bei Angabe eines Arrays alle zugehörigen Präfixe zurück.</span><span class="sxs-lookup"><span data-stu-id="c8307-105">Given an array, returns all its prefixes.</span></span>

```qsharp
function Prefixes<'T> (array : 'T[]) : 'T[][]
```


## <a name="description"></a><span data-ttu-id="c8307-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c8307-106">Description</span></span>

<span data-ttu-id="c8307-107">Gibt ein Array aller Präfixe zurück, beginnend mit einem Array, das nur das erste Element bis zum vollständigen Array enthält.</span><span class="sxs-lookup"><span data-stu-id="c8307-107">Returns an array of all prefixes, starting with an array that only has the first element until the complete array.</span></span>

## <a name="input"></a><span data-ttu-id="c8307-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c8307-108">Input</span></span>

### <a name="array--t"></a><span data-ttu-id="c8307-109">Array: 't []</span><span class="sxs-lookup"><span data-stu-id="c8307-109">array : 'T[]</span></span>

<span data-ttu-id="c8307-110">Ein Array von-Elementen.</span><span class="sxs-lookup"><span data-stu-id="c8307-110">An array of elements.</span></span>



## <a name="output--t"></a><span data-ttu-id="c8307-111">Ausgabe: 't [] []</span><span class="sxs-lookup"><span data-stu-id="c8307-111">Output : 'T[][]</span></span>



## <a name="type-parameters"></a><span data-ttu-id="c8307-112">Typparameter</span><span class="sxs-lookup"><span data-stu-id="c8307-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="c8307-113">GIF</span><span class="sxs-lookup"><span data-stu-id="c8307-113">'T</span></span>

<span data-ttu-id="c8307-114">Der Typ der `array` Elemente.</span><span class="sxs-lookup"><span data-stu-id="c8307-114">The type of `array` elements.</span></span>