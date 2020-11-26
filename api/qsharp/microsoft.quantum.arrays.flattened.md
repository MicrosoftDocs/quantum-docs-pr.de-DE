---
uid: Microsoft.Quantum.Arrays.Flattened
title: Vereinfachte Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Flattened
qsharp.summary: Given an array of arrays, returns the concatenation of all arrays.
ms.openlocfilehash: 331b1714109259b21982e99d030aa0662e3aaadb
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96221214"
---
# <a name="flattened-function"></a><span data-ttu-id="d01a2-102">Vereinfachte Funktion</span><span class="sxs-lookup"><span data-stu-id="d01a2-102">Flattened function</span></span>

<span data-ttu-id="d01a2-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="d01a2-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="d01a2-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="d01a2-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="d01a2-105">Gibt ein Array von Arrays zurück, das die Verkettung aller Arrays zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="d01a2-105">Given an array of arrays, returns the concatenation of all arrays.</span></span>

```qsharp
function Flattened<'T> (arrays : 'T[][]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="d01a2-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d01a2-106">Input</span></span>

### <a name="arrays--t"></a><span data-ttu-id="d01a2-107">Arrays: 't [] []</span><span class="sxs-lookup"><span data-stu-id="d01a2-107">arrays : 'T[][]</span></span>

<span data-ttu-id="d01a2-108">Array von Arrays.</span><span class="sxs-lookup"><span data-stu-id="d01a2-108">Array of arrays.</span></span>



## <a name="output--t"></a><span data-ttu-id="d01a2-109">Ausgabe: 't []</span><span class="sxs-lookup"><span data-stu-id="d01a2-109">Output : 'T[]</span></span>

<span data-ttu-id="d01a2-110">Verkettung aller Arrays.</span><span class="sxs-lookup"><span data-stu-id="d01a2-110">Concatenation of all arrays.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="d01a2-111">Typparameter</span><span class="sxs-lookup"><span data-stu-id="d01a2-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="d01a2-112">GIF</span><span class="sxs-lookup"><span data-stu-id="d01a2-112">'T</span></span>

<span data-ttu-id="d01a2-113">Der Typ der `array` Elemente.</span><span class="sxs-lookup"><span data-stu-id="d01a2-113">The type of `array` elements.</span></span>