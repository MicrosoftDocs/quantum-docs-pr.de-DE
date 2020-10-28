---
uid: Microsoft.Quantum.Arrays.Diagonal
title: Diagonal-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Diagonal
qsharp.summary: Returns an array of diagonal elements of a 2-dimensional array
ms.openlocfilehash: 180b7185c94d712fa02100cb97abfbb6c464d12a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706119"
---
# <a name="diagonal-function"></a><span data-ttu-id="ae3d9-102">Diagonal-Funktion</span><span class="sxs-lookup"><span data-stu-id="ae3d9-102">Diagonal function</span></span>

<span data-ttu-id="ae3d9-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="ae3d9-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="ae3d9-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="ae3d9-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="ae3d9-105">Gibt ein Array von diagonalen Elementen eines zweidimensionalen Arrays zurück.</span><span class="sxs-lookup"><span data-stu-id="ae3d9-105">Returns an array of diagonal elements of a 2-dimensional array</span></span>

```qsharp
function Diagonal<'T> (matrix : 'T[][]) : 'T[]
```


## <a name="description"></a><span data-ttu-id="ae3d9-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ae3d9-106">Description</span></span>

<span data-ttu-id="ae3d9-107">Wenn das zweidimensionale Array keine quadratische Form aufweist, wird die Diagonale über dem Minimalwert über der Anzahl von Zeilen und Spalten zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ae3d9-107">If the 2-dimensional array has not a square shape, the diagonal over the minimum over the number of rows and columns will be returned.</span></span>

## <a name="input"></a><span data-ttu-id="ae3d9-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ae3d9-108">Input</span></span>

### <a name="matrix--t"></a><span data-ttu-id="ae3d9-109">Matrix: 't [] []</span><span class="sxs-lookup"><span data-stu-id="ae3d9-109">matrix : 'T[][]</span></span>

<span data-ttu-id="ae3d9-110">zweidimensionale Matrix in Zeilen weiser Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="ae3d9-110">2-dimensional matrix in row-wise order</span></span>



## <a name="output--t"></a><span data-ttu-id="ae3d9-111">Ausgabe: 't []</span><span class="sxs-lookup"><span data-stu-id="ae3d9-111">Output : 'T[]</span></span>



## <a name="type-parameters"></a><span data-ttu-id="ae3d9-112">Typparameter</span><span class="sxs-lookup"><span data-stu-id="ae3d9-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="ae3d9-113">GIF</span><span class="sxs-lookup"><span data-stu-id="ae3d9-113">'T</span></span>

<span data-ttu-id="ae3d9-114">Der Typ der einzelnen Elemente von `matrix` .</span><span class="sxs-lookup"><span data-stu-id="ae3d9-114">The type of each element of `matrix`.</span></span>

## <a name="see-also"></a><span data-ttu-id="ae3d9-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ae3d9-115">See Also</span></span>

- [<span data-ttu-id="ae3d9-116">Microsoft. Quantum. Arrays. transferi</span><span class="sxs-lookup"><span data-stu-id="ae3d9-116">Microsoft.Quantum.Arrays.Transposed</span></span>](xref:Microsoft.Quantum.Arrays.Transposed)