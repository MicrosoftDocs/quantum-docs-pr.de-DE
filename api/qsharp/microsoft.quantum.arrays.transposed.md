---
uid: Microsoft.Quantum.Arrays.Transposed
title: Funktion wurde umgesetzt
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Transposed
qsharp.summary: Returns the transpose of a matrix represented as an array of arrays.
ms.openlocfilehash: 54071c461cf9f9411c332763b81e3bc448fb6c6e
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705738"
---
# <a name="transposed-function"></a><span data-ttu-id="23c7c-102">Funktion wurde umgesetzt</span><span class="sxs-lookup"><span data-stu-id="23c7c-102">Transposed function</span></span>

<span data-ttu-id="23c7c-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="23c7c-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="23c7c-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="23c7c-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="23c7c-105">Gibt das umsetzen einer Matrix zurück, die als Array von Arrays dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="23c7c-105">Returns the transpose of a matrix represented as an array of arrays.</span></span>

```qsharp
function Transposed<'T> (matrix : 'T[][]) : 'T[][]
```


## <a name="description"></a><span data-ttu-id="23c7c-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="23c7c-106">Description</span></span>

<span data-ttu-id="23c7c-107">Eingabe als $r \times c $ Matrix mit $r $ Rows und $c $ Columns.</span><span class="sxs-lookup"><span data-stu-id="23c7c-107">Input as an $r \times c$ matrix with $r$ rows and $c$ columns.</span></span>  <span data-ttu-id="23c7c-108">Die Matrix ist zeilenbasiert, d. h., es wird `matrix[i][j]` auf das Element in Zeile $i $ und Spalte $j $ zugegriffen.</span><span class="sxs-lookup"><span data-stu-id="23c7c-108">The matrix is row-based, i.e., `matrix[i][j]` accesses the element at row $i$ and column $j$.</span></span>

<span data-ttu-id="23c7c-109">Diese Funktion gibt die $c \times r $-Matrix zurück, die das umsetzen der Eingabe Matrix ist.</span><span class="sxs-lookup"><span data-stu-id="23c7c-109">This function returns the $c \times r$ matrix that is the transpose of the input matrix.</span></span>

## <a name="input"></a><span data-ttu-id="23c7c-110">Eingabe</span><span class="sxs-lookup"><span data-stu-id="23c7c-110">Input</span></span>

### <a name="matrix--t"></a><span data-ttu-id="23c7c-111">Matrix: 't [] []</span><span class="sxs-lookup"><span data-stu-id="23c7c-111">matrix : 'T[][]</span></span>

<span data-ttu-id="23c7c-112">Zeilen basiertes $r \times c $ Matrix</span><span class="sxs-lookup"><span data-stu-id="23c7c-112">Row-based $r \times c$ matrix</span></span>



## <a name="output--t"></a><span data-ttu-id="23c7c-113">Ausgabe: 't [] []</span><span class="sxs-lookup"><span data-stu-id="23c7c-113">Output : 'T[][]</span></span>

<span data-ttu-id="23c7c-114">Umgesetzte $c \times r $ Matrix</span><span class="sxs-lookup"><span data-stu-id="23c7c-114">Transposed $c \times r$ matrix</span></span>

## <a name="type-parameters"></a><span data-ttu-id="23c7c-115">Typparameter</span><span class="sxs-lookup"><span data-stu-id="23c7c-115">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="23c7c-116">GIF</span><span class="sxs-lookup"><span data-stu-id="23c7c-116">'T</span></span>

<span data-ttu-id="23c7c-117">Der Typ der einzelnen Elemente von `matrix` .</span><span class="sxs-lookup"><span data-stu-id="23c7c-117">The type of each element of `matrix`.</span></span>