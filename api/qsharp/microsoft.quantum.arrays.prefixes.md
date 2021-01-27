---
uid: Microsoft.Quantum.Arrays.Prefixes
title: Präfixe-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Prefixes
qsharp.summary: Given an array, returns all its prefixes.
ms.openlocfilehash: a2e1721f8f59bf9aa425f04710637023d482a2ca
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845514"
---
# <a name="prefixes-function"></a><span data-ttu-id="f49d2-102">Präfixe-Funktion</span><span class="sxs-lookup"><span data-stu-id="f49d2-102">Prefixes function</span></span>

<span data-ttu-id="f49d2-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="f49d2-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="f49d2-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="f49d2-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="f49d2-105">Gibt bei Angabe eines Arrays alle zugehörigen Präfixe zurück.</span><span class="sxs-lookup"><span data-stu-id="f49d2-105">Given an array, returns all its prefixes.</span></span>

```qsharp
function Prefixes<'T> (array : 'T[]) : 'T[][]
```


## <a name="description"></a><span data-ttu-id="f49d2-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f49d2-106">Description</span></span>

<span data-ttu-id="f49d2-107">Gibt ein Array aller Präfixe zurück, beginnend mit einem Array, das nur das erste Element bis zum vollständigen Array enthält.</span><span class="sxs-lookup"><span data-stu-id="f49d2-107">Returns an array of all prefixes, starting with an array that only has the first element until the complete array.</span></span>

## <a name="input"></a><span data-ttu-id="f49d2-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f49d2-108">Input</span></span>

### <a name="array--t"></a><span data-ttu-id="f49d2-109">Array: 't []</span><span class="sxs-lookup"><span data-stu-id="f49d2-109">array : 'T[]</span></span>

<span data-ttu-id="f49d2-110">Ein Array von-Elementen.</span><span class="sxs-lookup"><span data-stu-id="f49d2-110">An array of elements.</span></span>



## <a name="output--t"></a><span data-ttu-id="f49d2-111">Ausgabe: 't [] []</span><span class="sxs-lookup"><span data-stu-id="f49d2-111">Output : 'T[][]</span></span>



## <a name="type-parameters"></a><span data-ttu-id="f49d2-112">Typparameter</span><span class="sxs-lookup"><span data-stu-id="f49d2-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="f49d2-113">GIF</span><span class="sxs-lookup"><span data-stu-id="f49d2-113">'T</span></span>

<span data-ttu-id="f49d2-114">Der Typ der `array` Elemente.</span><span class="sxs-lookup"><span data-stu-id="f49d2-114">The type of `array` elements.</span></span>

## <a name="example"></a><span data-ttu-id="f49d2-115">Beispiel</span><span class="sxs-lookup"><span data-stu-id="f49d2-115">Example</span></span>

```qsharp
let prefixes = Prefixes([23, 42, 144]);
// prefixes = [[23], [23, 42], [23, 42, 144]]
```