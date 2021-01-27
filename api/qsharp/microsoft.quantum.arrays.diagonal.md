---
uid: Microsoft.Quantum.Arrays.Diagonal
title: Diagonal-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Diagonal
qsharp.summary: Returns an array of diagonal elements of a 2-dimensional array
ms.openlocfilehash: 2857046f59a958fed106af0944b75baaa3292e96
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842823"
---
# <a name="diagonal-function"></a><span data-ttu-id="ffbff-102">Diagonal-Funktion</span><span class="sxs-lookup"><span data-stu-id="ffbff-102">Diagonal function</span></span>

<span data-ttu-id="ffbff-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="ffbff-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="ffbff-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="ffbff-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="ffbff-105">Gibt ein Array von diagonalen Elementen eines zweidimensionalen Arrays zurück.</span><span class="sxs-lookup"><span data-stu-id="ffbff-105">Returns an array of diagonal elements of a 2-dimensional array</span></span>

```qsharp
function Diagonal<'T> (matrix : 'T[][]) : 'T[]
```


## <a name="description"></a><span data-ttu-id="ffbff-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ffbff-106">Description</span></span>

<span data-ttu-id="ffbff-107">Wenn das zweidimensionale Array keine quadratische Form aufweist, wird die Diagonale über dem Minimalwert über der Anzahl von Zeilen und Spalten zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ffbff-107">If the 2-dimensional array has not a square shape, the diagonal over the minimum over the number of rows and columns will be returned.</span></span>

## <a name="input"></a><span data-ttu-id="ffbff-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ffbff-108">Input</span></span>

### <a name="matrix--t"></a><span data-ttu-id="ffbff-109">Matrix: 't [] []</span><span class="sxs-lookup"><span data-stu-id="ffbff-109">matrix : 'T[][]</span></span>

<span data-ttu-id="ffbff-110">zweidimensionale Matrix in Zeilen weiser Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="ffbff-110">2-dimensional matrix in row-wise order</span></span>



## <a name="output--t"></a><span data-ttu-id="ffbff-111">Ausgabe: 't []</span><span class="sxs-lookup"><span data-stu-id="ffbff-111">Output : 'T[]</span></span>



## <a name="type-parameters"></a><span data-ttu-id="ffbff-112">Typparameter</span><span class="sxs-lookup"><span data-stu-id="ffbff-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="ffbff-113">GIF</span><span class="sxs-lookup"><span data-stu-id="ffbff-113">'T</span></span>

<span data-ttu-id="ffbff-114">Der Typ der einzelnen Elemente von `matrix` .</span><span class="sxs-lookup"><span data-stu-id="ffbff-114">The type of each element of `matrix`.</span></span>

## <a name="example"></a><span data-ttu-id="ffbff-115">Beispiel</span><span class="sxs-lookup"><span data-stu-id="ffbff-115">Example</span></span>

```qsharp
let matrix = [[1, 2, 3], [4, 5, 6], [7, 8, 9]];
let diagonal = Diagonal(matrix);
// same as: column = [1, 5, 9]
```

## <a name="see-also"></a><span data-ttu-id="ffbff-116">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ffbff-116">See Also</span></span>

- [<span data-ttu-id="ffbff-117">Microsoft. Quantum. Arrays. transferi</span><span class="sxs-lookup"><span data-stu-id="ffbff-117">Microsoft.Quantum.Arrays.Transposed</span></span>](xref:Microsoft.Quantum.Arrays.Transposed)