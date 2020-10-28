---
uid: Microsoft.Quantum.Arrays.Flattened
title: Vereinfachte Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Flattened
qsharp.summary: Given an array of arrays, returns the concatenation of all arrays.
ms.openlocfilehash: 91a35f0ac2c2f8609bac07734265fcf4e88bf50b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706023"
---
# <a name="flattened-function"></a><span data-ttu-id="aea0a-102">Vereinfachte Funktion</span><span class="sxs-lookup"><span data-stu-id="aea0a-102">Flattened function</span></span>

<span data-ttu-id="aea0a-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="aea0a-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="aea0a-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="aea0a-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="aea0a-105">Gibt ein Array von Arrays zurück, das die Verkettung aller Arrays zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="aea0a-105">Given an array of arrays, returns the concatenation of all arrays.</span></span>

```qsharp
function Flattened<'T> (arrays : 'T[][]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="aea0a-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="aea0a-106">Input</span></span>

### <a name="arrays--t"></a><span data-ttu-id="aea0a-107">Arrays: 't [] []</span><span class="sxs-lookup"><span data-stu-id="aea0a-107">arrays : 'T[][]</span></span>

<span data-ttu-id="aea0a-108">Array von Arrays.</span><span class="sxs-lookup"><span data-stu-id="aea0a-108">Array of arrays.</span></span>



## <a name="output--t"></a><span data-ttu-id="aea0a-109">Ausgabe: 't []</span><span class="sxs-lookup"><span data-stu-id="aea0a-109">Output : 'T[]</span></span>

<span data-ttu-id="aea0a-110">Verkettung aller Arrays.</span><span class="sxs-lookup"><span data-stu-id="aea0a-110">Concatenation of all arrays.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="aea0a-111">Typparameter</span><span class="sxs-lookup"><span data-stu-id="aea0a-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="aea0a-112">GIF</span><span class="sxs-lookup"><span data-stu-id="aea0a-112">'T</span></span>

<span data-ttu-id="aea0a-113">Der Typ der `array` Elemente.</span><span class="sxs-lookup"><span data-stu-id="aea0a-113">The type of `array` elements.</span></span>