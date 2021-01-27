---
uid: Microsoft.Quantum.Arrays.Flattened
title: Vereinfachte Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Flattened
qsharp.summary: Given an array of arrays, returns the concatenation of all arrays.
ms.openlocfilehash: 272533d4efd8598b21daa341c867c070a2083ce0
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848619"
---
# <a name="flattened-function"></a><span data-ttu-id="7d2db-102">Vereinfachte Funktion</span><span class="sxs-lookup"><span data-stu-id="7d2db-102">Flattened function</span></span>

<span data-ttu-id="7d2db-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="7d2db-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="7d2db-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="7d2db-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="7d2db-105">Gibt ein Array von Arrays zurück, das die Verkettung aller Arrays zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="7d2db-105">Given an array of arrays, returns the concatenation of all arrays.</span></span>

```qsharp
function Flattened<'T> (arrays : 'T[][]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="7d2db-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="7d2db-106">Input</span></span>

### <a name="arrays--t"></a><span data-ttu-id="7d2db-107">Arrays: 't [] []</span><span class="sxs-lookup"><span data-stu-id="7d2db-107">arrays : 'T[][]</span></span>

<span data-ttu-id="7d2db-108">Array von Arrays.</span><span class="sxs-lookup"><span data-stu-id="7d2db-108">Array of arrays.</span></span>



## <a name="output--t"></a><span data-ttu-id="7d2db-109">Ausgabe: 't []</span><span class="sxs-lookup"><span data-stu-id="7d2db-109">Output : 'T[]</span></span>

<span data-ttu-id="7d2db-110">Verkettung aller Arrays.</span><span class="sxs-lookup"><span data-stu-id="7d2db-110">Concatenation of all arrays.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="7d2db-111">Typparameter</span><span class="sxs-lookup"><span data-stu-id="7d2db-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="7d2db-112">GIF</span><span class="sxs-lookup"><span data-stu-id="7d2db-112">'T</span></span>

<span data-ttu-id="7d2db-113">Der Typ der `array` Elemente.</span><span class="sxs-lookup"><span data-stu-id="7d2db-113">The type of `array` elements.</span></span>

## <a name="example"></a><span data-ttu-id="7d2db-114">Beispiel</span><span class="sxs-lookup"><span data-stu-id="7d2db-114">Example</span></span>

```qsharp
let flattened = Flattened([[1, 2], [3], [4, 5, 6]]);
// flattened = [1, 2, 3, 4, 5, 6]
```