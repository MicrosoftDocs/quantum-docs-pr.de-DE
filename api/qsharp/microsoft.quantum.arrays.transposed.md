---
uid: Microsoft.Quantum.Arrays.Transposed
title: Funktion wurde umgesetzt
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Transposed
qsharp.summary: Returns the transpose of a matrix represented as an array of arrays.
ms.openlocfilehash: 913f1829ef53ec3eb6944be8b8e3eb37b431f27e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850933"
---
# <a name="transposed-function"></a><span data-ttu-id="42c69-102">Funktion wurde umgesetzt</span><span class="sxs-lookup"><span data-stu-id="42c69-102">Transposed function</span></span>

<span data-ttu-id="42c69-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="42c69-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="42c69-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="42c69-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="42c69-105">Gibt das umsetzen einer Matrix zurück, die als Array von Arrays dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="42c69-105">Returns the transpose of a matrix represented as an array of arrays.</span></span>

```qsharp
function Transposed<'T> (matrix : 'T[][]) : 'T[][]
```


## <a name="description"></a><span data-ttu-id="42c69-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="42c69-106">Description</span></span>

<span data-ttu-id="42c69-107">Eingabe als $r \times c $ Matrix mit $r $ Rows und $c $ Columns.</span><span class="sxs-lookup"><span data-stu-id="42c69-107">Input as an $r \times c$ matrix with $r$ rows and $c$ columns.</span></span>  <span data-ttu-id="42c69-108">Die Matrix ist zeilenbasiert, d. h., es wird `matrix[i][j]` auf das Element in Zeile $i $ und Spalte $j $ zugegriffen.</span><span class="sxs-lookup"><span data-stu-id="42c69-108">The matrix is row-based, i.e., `matrix[i][j]` accesses the element at row $i$ and column $j$.</span></span>

<span data-ttu-id="42c69-109">Diese Funktion gibt die $c \times r $-Matrix zurück, die das umsetzen der Eingabe Matrix ist.</span><span class="sxs-lookup"><span data-stu-id="42c69-109">This function returns the $c \times r$ matrix that is the transpose of the input matrix.</span></span>

## <a name="input"></a><span data-ttu-id="42c69-110">Eingabe</span><span class="sxs-lookup"><span data-stu-id="42c69-110">Input</span></span>

### <a name="matrix--t"></a><span data-ttu-id="42c69-111">Matrix: 't [] []</span><span class="sxs-lookup"><span data-stu-id="42c69-111">matrix : 'T[][]</span></span>

<span data-ttu-id="42c69-112">Zeilen basiertes $r \times c $ Matrix</span><span class="sxs-lookup"><span data-stu-id="42c69-112">Row-based $r \times c$ matrix</span></span>



## <a name="output--t"></a><span data-ttu-id="42c69-113">Ausgabe: 't [] []</span><span class="sxs-lookup"><span data-stu-id="42c69-113">Output : 'T[][]</span></span>

<span data-ttu-id="42c69-114">Umgesetzte $c \times r $ Matrix</span><span class="sxs-lookup"><span data-stu-id="42c69-114">Transposed $c \times r$ matrix</span></span>

## <a name="type-parameters"></a><span data-ttu-id="42c69-115">Typparameter</span><span class="sxs-lookup"><span data-stu-id="42c69-115">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="42c69-116">GIF</span><span class="sxs-lookup"><span data-stu-id="42c69-116">'T</span></span>

<span data-ttu-id="42c69-117">Der Typ der einzelnen Elemente von `matrix` .</span><span class="sxs-lookup"><span data-stu-id="42c69-117">The type of each element of `matrix`.</span></span>

## <a name="example"></a><span data-ttu-id="42c69-118">Beispiel</span><span class="sxs-lookup"><span data-stu-id="42c69-118">Example</span></span>

```qsharp
// same as [[1, 4], [2, 5], [3, 6]]
let transposed = Transposed([[1, 2, 3], [4, 5, 6]]);
```