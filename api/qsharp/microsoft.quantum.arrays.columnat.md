---
uid: Microsoft.Quantum.Arrays.ColumnAt
title: Columnat-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: ColumnAt
qsharp.summary: Extracts a column from a matrix.
ms.openlocfilehash: 097b3fdd6fc1843ada27052fcf08ee80d894d25a
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96210097"
---
# <a name="columnat-function"></a><span data-ttu-id="b3592-102">Columnat-Funktion</span><span class="sxs-lookup"><span data-stu-id="b3592-102">ColumnAt function</span></span>

<span data-ttu-id="b3592-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="b3592-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="b3592-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="b3592-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="b3592-105">Extrahiert eine Spalte aus einer Matrix.</span><span class="sxs-lookup"><span data-stu-id="b3592-105">Extracts a column from a matrix.</span></span>

```qsharp
function ColumnAt<'T> (column : Int, matrix : 'T[][]) : 'T[]
```


## <a name="description"></a><span data-ttu-id="b3592-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b3592-106">Description</span></span>

<span data-ttu-id="b3592-107">Diese Funktion extrahiert eine Spalte in einer Matrix in Zeilen weiser Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="b3592-107">This function extracts a column in a matrix in row-wise order.</span></span>
<span data-ttu-id="b3592-108">Extrahieren einer Zeile ("corrsponds") für den Element Zugriff auf den ersten Index und erfordert daher keine weitere Behandlung.</span><span class="sxs-lookup"><span data-stu-id="b3592-108">Extracting a row corrsponds to element access of the first index and therefore requires no further treatment.</span></span>

## <a name="input"></a><span data-ttu-id="b3592-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b3592-109">Input</span></span>

### <a name="column--int"></a><span data-ttu-id="b3592-110">Spalte: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="b3592-110">column : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="b3592-111">Spalte der Matrix</span><span class="sxs-lookup"><span data-stu-id="b3592-111">Column of the matrix</span></span>


### <a name="matrix--t"></a><span data-ttu-id="b3592-112">Matrix: 't [] []</span><span class="sxs-lookup"><span data-stu-id="b3592-112">matrix : 'T[][]</span></span>

<span data-ttu-id="b3592-113">zweidimensionale Matrix in Zeilen weiser Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="b3592-113">2-dimensional matrix in row-wise order</span></span>



## <a name="output--t"></a><span data-ttu-id="b3592-114">Ausgabe: 't []</span><span class="sxs-lookup"><span data-stu-id="b3592-114">Output : 'T[]</span></span>



## <a name="type-parameters"></a><span data-ttu-id="b3592-115">Typparameter</span><span class="sxs-lookup"><span data-stu-id="b3592-115">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="b3592-116">GIF</span><span class="sxs-lookup"><span data-stu-id="b3592-116">'T</span></span>

<span data-ttu-id="b3592-117">Der Typ der einzelnen Elemente von `matrix` .</span><span class="sxs-lookup"><span data-stu-id="b3592-117">The type of each element of `matrix`.</span></span>

## <a name="see-also"></a><span data-ttu-id="b3592-118">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b3592-118">See Also</span></span>

- [<span data-ttu-id="b3592-119">Microsoft. Quantum. Arrays. transferi</span><span class="sxs-lookup"><span data-stu-id="b3592-119">Microsoft.Quantum.Arrays.Transposed</span></span>](xref:Microsoft.Quantum.Arrays.Transposed)
- [<span data-ttu-id="b3592-120">Microsoft. Quantum. Arrays. Diagonal</span><span class="sxs-lookup"><span data-stu-id="b3592-120">Microsoft.Quantum.Arrays.Diagonal</span></span>](xref:Microsoft.Quantum.Arrays.Diagonal)