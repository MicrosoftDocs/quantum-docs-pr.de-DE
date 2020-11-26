---
uid: Microsoft.Quantum.Arrays.Transposed
title: Funktion wurde umgesetzt
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Transposed
qsharp.summary: Returns the transpose of a matrix represented as an array of arrays.
ms.openlocfilehash: f293399d8e3a2cb32b2929e8d1591ac5eaefd277
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96219990"
---
# <a name="transposed-function"></a><span data-ttu-id="a5244-102">Funktion wurde umgesetzt</span><span class="sxs-lookup"><span data-stu-id="a5244-102">Transposed function</span></span>

<span data-ttu-id="a5244-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="a5244-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="a5244-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a5244-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="a5244-105">Gibt das umsetzen einer Matrix zurück, die als Array von Arrays dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="a5244-105">Returns the transpose of a matrix represented as an array of arrays.</span></span>

```qsharp
function Transposed<'T> (matrix : 'T[][]) : 'T[][]
```


## <a name="description"></a><span data-ttu-id="a5244-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a5244-106">Description</span></span>

<span data-ttu-id="a5244-107">Eingabe als $r \times c $ Matrix mit $r $ Rows und $c $ Columns.</span><span class="sxs-lookup"><span data-stu-id="a5244-107">Input as an $r \times c$ matrix with $r$ rows and $c$ columns.</span></span>  <span data-ttu-id="a5244-108">Die Matrix ist zeilenbasiert, d. h., es wird `matrix[i][j]` auf das Element in Zeile $i $ und Spalte $j $ zugegriffen.</span><span class="sxs-lookup"><span data-stu-id="a5244-108">The matrix is row-based, i.e., `matrix[i][j]` accesses the element at row $i$ and column $j$.</span></span>

<span data-ttu-id="a5244-109">Diese Funktion gibt die $c \times r $-Matrix zurück, die das umsetzen der Eingabe Matrix ist.</span><span class="sxs-lookup"><span data-stu-id="a5244-109">This function returns the $c \times r$ matrix that is the transpose of the input matrix.</span></span>

## <a name="input"></a><span data-ttu-id="a5244-110">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a5244-110">Input</span></span>

### <a name="matrix--t"></a><span data-ttu-id="a5244-111">Matrix: 't [] []</span><span class="sxs-lookup"><span data-stu-id="a5244-111">matrix : 'T[][]</span></span>

<span data-ttu-id="a5244-112">Zeilen basiertes $r \times c $ Matrix</span><span class="sxs-lookup"><span data-stu-id="a5244-112">Row-based $r \times c$ matrix</span></span>



## <a name="output--t"></a><span data-ttu-id="a5244-113">Ausgabe: 't [] []</span><span class="sxs-lookup"><span data-stu-id="a5244-113">Output : 'T[][]</span></span>

<span data-ttu-id="a5244-114">Umgesetzte $c \times r $ Matrix</span><span class="sxs-lookup"><span data-stu-id="a5244-114">Transposed $c \times r$ matrix</span></span>

## <a name="type-parameters"></a><span data-ttu-id="a5244-115">Typparameter</span><span class="sxs-lookup"><span data-stu-id="a5244-115">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="a5244-116">GIF</span><span class="sxs-lookup"><span data-stu-id="a5244-116">'T</span></span>

<span data-ttu-id="a5244-117">Der Typ der einzelnen Elemente von `matrix` .</span><span class="sxs-lookup"><span data-stu-id="a5244-117">The type of each element of `matrix`.</span></span>