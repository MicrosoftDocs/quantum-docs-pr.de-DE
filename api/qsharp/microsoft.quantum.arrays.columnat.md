---
uid: Microsoft.Quantum.Arrays.ColumnAt
title: Columnat-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: ColumnAt
qsharp.summary: Extracts a column from a matrix.
ms.openlocfilehash: ad09ada1a2253a54e70dddd6dba8aa243d2cd5a6
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706167"
---
# <a name="columnat-function"></a><span data-ttu-id="d6ef4-102">Columnat-Funktion</span><span class="sxs-lookup"><span data-stu-id="d6ef4-102">ColumnAt function</span></span>

<span data-ttu-id="d6ef4-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="d6ef4-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="d6ef4-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="d6ef4-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="d6ef4-105">Extrahiert eine Spalte aus einer Matrix.</span><span class="sxs-lookup"><span data-stu-id="d6ef4-105">Extracts a column from a matrix.</span></span>

```qsharp
function ColumnAt<'T> (column : Int, matrix : 'T[][]) : 'T[]
```


## <a name="description"></a><span data-ttu-id="d6ef4-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d6ef4-106">Description</span></span>

<span data-ttu-id="d6ef4-107">Diese Funktion extrahiert eine Spalte in einer Matrix in Zeilen weiser Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="d6ef4-107">This function extracts a column in a matrix in row-wise order.</span></span>
<span data-ttu-id="d6ef4-108">Extrahieren einer Zeile ("corrsponds") für den Element Zugriff auf den ersten Index und erfordert daher keine weitere Behandlung.</span><span class="sxs-lookup"><span data-stu-id="d6ef4-108">Extracting a row corrsponds to element access of the first index and therefore requires no further treatment.</span></span>

## <a name="input"></a><span data-ttu-id="d6ef4-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d6ef4-109">Input</span></span>

### <a name="column--int"></a><span data-ttu-id="d6ef4-110">Spalte: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="d6ef4-110">column : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="d6ef4-111">Spalte der Matrix</span><span class="sxs-lookup"><span data-stu-id="d6ef4-111">Column of the matrix</span></span>


### <a name="matrix--t"></a><span data-ttu-id="d6ef4-112">Matrix: 't [] []</span><span class="sxs-lookup"><span data-stu-id="d6ef4-112">matrix : 'T[][]</span></span>

<span data-ttu-id="d6ef4-113">zweidimensionale Matrix in Zeilen weiser Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="d6ef4-113">2-dimensional matrix in row-wise order</span></span>



## <a name="output--t"></a><span data-ttu-id="d6ef4-114">Ausgabe: 't []</span><span class="sxs-lookup"><span data-stu-id="d6ef4-114">Output : 'T[]</span></span>



## <a name="type-parameters"></a><span data-ttu-id="d6ef4-115">Typparameter</span><span class="sxs-lookup"><span data-stu-id="d6ef4-115">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="d6ef4-116">GIF</span><span class="sxs-lookup"><span data-stu-id="d6ef4-116">'T</span></span>

<span data-ttu-id="d6ef4-117">Der Typ der einzelnen Elemente von `matrix` .</span><span class="sxs-lookup"><span data-stu-id="d6ef4-117">The type of each element of `matrix`.</span></span>

## <a name="see-also"></a><span data-ttu-id="d6ef4-118">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="d6ef4-118">See Also</span></span>

- [<span data-ttu-id="d6ef4-119">Microsoft. Quantum. Arrays. transferi</span><span class="sxs-lookup"><span data-stu-id="d6ef4-119">Microsoft.Quantum.Arrays.Transposed</span></span>](xref:Microsoft.Quantum.Arrays.Transposed)
- [<span data-ttu-id="d6ef4-120">Microsoft. Quantum. Arrays. Diagonal</span><span class="sxs-lookup"><span data-stu-id="d6ef4-120">Microsoft.Quantum.Arrays.Diagonal</span></span>](xref:Microsoft.Quantum.Arrays.Diagonal)