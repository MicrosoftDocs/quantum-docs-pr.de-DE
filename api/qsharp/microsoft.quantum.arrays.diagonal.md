---
uid: Microsoft.Quantum.Arrays.Diagonal
title: Diagonal-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Diagonal
qsharp.summary: Returns an array of diagonal elements of a 2-dimensional array
ms.openlocfilehash: fe6bac0acfa07b14620c7c35ae5e1cec2287d13d
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96221537"
---
# <a name="diagonal-function"></a><span data-ttu-id="0fef5-102">Diagonal-Funktion</span><span class="sxs-lookup"><span data-stu-id="0fef5-102">Diagonal function</span></span>

<span data-ttu-id="0fef5-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="0fef5-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="0fef5-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="0fef5-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="0fef5-105">Gibt ein Array von diagonalen Elementen eines zweidimensionalen Arrays zurück.</span><span class="sxs-lookup"><span data-stu-id="0fef5-105">Returns an array of diagonal elements of a 2-dimensional array</span></span>

```qsharp
function Diagonal<'T> (matrix : 'T[][]) : 'T[]
```


## <a name="description"></a><span data-ttu-id="0fef5-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0fef5-106">Description</span></span>

<span data-ttu-id="0fef5-107">Wenn das zweidimensionale Array keine quadratische Form aufweist, wird die Diagonale über dem Minimalwert über der Anzahl von Zeilen und Spalten zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="0fef5-107">If the 2-dimensional array has not a square shape, the diagonal over the minimum over the number of rows and columns will be returned.</span></span>

## <a name="input"></a><span data-ttu-id="0fef5-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0fef5-108">Input</span></span>

### <a name="matrix--t"></a><span data-ttu-id="0fef5-109">Matrix: 't [] []</span><span class="sxs-lookup"><span data-stu-id="0fef5-109">matrix : 'T[][]</span></span>

<span data-ttu-id="0fef5-110">zweidimensionale Matrix in Zeilen weiser Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="0fef5-110">2-dimensional matrix in row-wise order</span></span>



## <a name="output--t"></a><span data-ttu-id="0fef5-111">Ausgabe: 't []</span><span class="sxs-lookup"><span data-stu-id="0fef5-111">Output : 'T[]</span></span>



## <a name="type-parameters"></a><span data-ttu-id="0fef5-112">Typparameter</span><span class="sxs-lookup"><span data-stu-id="0fef5-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="0fef5-113">GIF</span><span class="sxs-lookup"><span data-stu-id="0fef5-113">'T</span></span>

<span data-ttu-id="0fef5-114">Der Typ der einzelnen Elemente von `matrix` .</span><span class="sxs-lookup"><span data-stu-id="0fef5-114">The type of each element of `matrix`.</span></span>

## <a name="see-also"></a><span data-ttu-id="0fef5-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="0fef5-115">See Also</span></span>

- [<span data-ttu-id="0fef5-116">Microsoft. Quantum. Arrays. transferi</span><span class="sxs-lookup"><span data-stu-id="0fef5-116">Microsoft.Quantum.Arrays.Transposed</span></span>](xref:Microsoft.Quantum.Arrays.Transposed)