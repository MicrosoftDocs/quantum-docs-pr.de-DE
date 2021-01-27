---
uid: Microsoft.Quantum.Arrays.ColumnAtUnchecked
title: Columnatdeaktiviert-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: ColumnAtUnchecked
qsharp.summary: This function does not check for matrix shape
ms.openlocfilehash: 4f4631bb49f769816a3df772f7b2f346c8ccfc78
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842860"
---
# <a name="columnatunchecked-function"></a><span data-ttu-id="9bc44-102">Columnatdeaktiviert-Funktion</span><span class="sxs-lookup"><span data-stu-id="9bc44-102">ColumnAtUnchecked function</span></span>

<span data-ttu-id="9bc44-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="9bc44-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="9bc44-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="9bc44-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="9bc44-105">Diese Funktion prüft nicht die Form "Matrix".</span><span class="sxs-lookup"><span data-stu-id="9bc44-105">This function does not check for matrix shape</span></span>

```qsharp
function ColumnAtUnchecked<'T> (column : Int, matrix : 'T[][]) : 'T[]
```


## <a name="description"></a><span data-ttu-id="9bc44-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9bc44-106">Description</span></span>

<span data-ttu-id="9bc44-107">Diese Funktion kann in anderen mehrdimensionalen Funktionen verwendet werden, die die Eingabe Matrix bereits auf eine gültige rechteckige Form überprüft haben.</span><span class="sxs-lookup"><span data-stu-id="9bc44-107">This function can be used in other multidimensional functions, which already check the input matrix for a valid rectangular shape.</span></span>

## <a name="input"></a><span data-ttu-id="9bc44-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="9bc44-108">Input</span></span>

### <a name="column--int"></a><span data-ttu-id="9bc44-109">Spalte: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="9bc44-109">column : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>




### <a name="matrix--t"></a><span data-ttu-id="9bc44-110">Matrix: 't [] []</span><span class="sxs-lookup"><span data-stu-id="9bc44-110">matrix : 'T[][]</span></span>





## <a name="output--t"></a><span data-ttu-id="9bc44-111">Ausgabe: 't []</span><span class="sxs-lookup"><span data-stu-id="9bc44-111">Output : 'T[]</span></span>



## <a name="type-parameters"></a><span data-ttu-id="9bc44-112">Typparameter</span><span class="sxs-lookup"><span data-stu-id="9bc44-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="9bc44-113">GIF</span><span class="sxs-lookup"><span data-stu-id="9bc44-113">'T</span></span>

