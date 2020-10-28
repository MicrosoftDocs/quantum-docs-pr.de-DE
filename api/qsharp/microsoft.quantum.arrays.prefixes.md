---
uid: Microsoft.Quantum.Arrays.Prefixes
title: Präfixe-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Prefixes
qsharp.summary: Given an array, returns all its prefixes.
ms.openlocfilehash: 1576e57e9dc64a605eb65cb841640e72a3b126ab
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705823"
---
# <a name="prefixes-function"></a><span data-ttu-id="9adad-102">Präfixe-Funktion</span><span class="sxs-lookup"><span data-stu-id="9adad-102">Prefixes function</span></span>

<span data-ttu-id="9adad-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="9adad-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="9adad-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="9adad-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="9adad-105">Gibt bei Angabe eines Arrays alle zugehörigen Präfixe zurück.</span><span class="sxs-lookup"><span data-stu-id="9adad-105">Given an array, returns all its prefixes.</span></span>

```qsharp
function Prefixes<'T> (array : 'T[]) : 'T[][]
```


## <a name="description"></a><span data-ttu-id="9adad-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9adad-106">Description</span></span>

<span data-ttu-id="9adad-107">Gibt ein Array aller Präfixe zurück, beginnend mit einem Array, das nur das erste Element bis zum vollständigen Array enthält.</span><span class="sxs-lookup"><span data-stu-id="9adad-107">Returns an array of all prefixes, starting with an array that only has the first element until the complete array.</span></span>

## <a name="input"></a><span data-ttu-id="9adad-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="9adad-108">Input</span></span>

### <a name="array--t"></a><span data-ttu-id="9adad-109">Array: 't []</span><span class="sxs-lookup"><span data-stu-id="9adad-109">array : 'T[]</span></span>

<span data-ttu-id="9adad-110">Ein Array von-Elementen.</span><span class="sxs-lookup"><span data-stu-id="9adad-110">An array of elements.</span></span>



## <a name="output--t"></a><span data-ttu-id="9adad-111">Ausgabe: 't [] []</span><span class="sxs-lookup"><span data-stu-id="9adad-111">Output : 'T[][]</span></span>



## <a name="type-parameters"></a><span data-ttu-id="9adad-112">Typparameter</span><span class="sxs-lookup"><span data-stu-id="9adad-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="9adad-113">GIF</span><span class="sxs-lookup"><span data-stu-id="9adad-113">'T</span></span>

<span data-ttu-id="9adad-114">Der Typ der `array` Elemente.</span><span class="sxs-lookup"><span data-stu-id="9adad-114">The type of `array` elements.</span></span>