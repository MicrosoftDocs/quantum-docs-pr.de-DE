---
uid: Microsoft.Quantum.Arrays.ColumnAt
title: Columnat-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: ColumnAt
qsharp.summary: Extracts a column from a matrix.
ms.openlocfilehash: 32dc814de9b04563c2798a768f121723a1a8252c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846260"
---
# <a name="columnat-function"></a><span data-ttu-id="cdd91-102">Columnat-Funktion</span><span class="sxs-lookup"><span data-stu-id="cdd91-102">ColumnAt function</span></span>

<span data-ttu-id="cdd91-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="cdd91-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="cdd91-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="cdd91-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="cdd91-105">Extrahiert eine Spalte aus einer Matrix.</span><span class="sxs-lookup"><span data-stu-id="cdd91-105">Extracts a column from a matrix.</span></span>

```qsharp
function ColumnAt<'T> (column : Int, matrix : 'T[][]) : 'T[]
```


## <a name="description"></a><span data-ttu-id="cdd91-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cdd91-106">Description</span></span>

<span data-ttu-id="cdd91-107">Diese Funktion extrahiert eine Spalte in einer Matrix in Zeilen weiser Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="cdd91-107">This function extracts a column in a matrix in row-wise order.</span></span>
<span data-ttu-id="cdd91-108">Extrahieren einer Zeile ("corrsponds") für den Element Zugriff auf den ersten Index und erfordert daher keine weitere Behandlung.</span><span class="sxs-lookup"><span data-stu-id="cdd91-108">Extracting a row corrsponds to element access of the first index and therefore requires no further treatment.</span></span>

## <a name="input"></a><span data-ttu-id="cdd91-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="cdd91-109">Input</span></span>

### <a name="column--int"></a><span data-ttu-id="cdd91-110">Spalte: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="cdd91-110">column : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="cdd91-111">Spalte der Matrix</span><span class="sxs-lookup"><span data-stu-id="cdd91-111">Column of the matrix</span></span>


### <a name="matrix--t"></a><span data-ttu-id="cdd91-112">Matrix: 't [] []</span><span class="sxs-lookup"><span data-stu-id="cdd91-112">matrix : 'T[][]</span></span>

<span data-ttu-id="cdd91-113">zweidimensionale Matrix in Zeilen weiser Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="cdd91-113">2-dimensional matrix in row-wise order</span></span>



## <a name="output--t"></a><span data-ttu-id="cdd91-114">Ausgabe: 't []</span><span class="sxs-lookup"><span data-stu-id="cdd91-114">Output : 'T[]</span></span>



## <a name="type-parameters"></a><span data-ttu-id="cdd91-115">Typparameter</span><span class="sxs-lookup"><span data-stu-id="cdd91-115">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="cdd91-116">GIF</span><span class="sxs-lookup"><span data-stu-id="cdd91-116">'T</span></span>

<span data-ttu-id="cdd91-117">Der Typ der einzelnen Elemente von `matrix` .</span><span class="sxs-lookup"><span data-stu-id="cdd91-117">The type of each element of `matrix`.</span></span>

## <a name="example"></a><span data-ttu-id="cdd91-118">Beispiel</span><span class="sxs-lookup"><span data-stu-id="cdd91-118">Example</span></span>

```qsharp
let matrix = [[1, 2, 3], [4, 5, 6], [7, 8, 9]];
let column = ColumnAt(0, matrix);
// same as: column = [1, 4, 7]
```

## <a name="see-also"></a><span data-ttu-id="cdd91-119">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="cdd91-119">See Also</span></span>

- [<span data-ttu-id="cdd91-120">Microsoft. Quantum. Arrays. transferi</span><span class="sxs-lookup"><span data-stu-id="cdd91-120">Microsoft.Quantum.Arrays.Transposed</span></span>](xref:Microsoft.Quantum.Arrays.Transposed)
- [<span data-ttu-id="cdd91-121">Microsoft. Quantum. Arrays. Diagonal</span><span class="sxs-lookup"><span data-stu-id="cdd91-121">Microsoft.Quantum.Arrays.Diagonal</span></span>](xref:Microsoft.Quantum.Arrays.Diagonal)