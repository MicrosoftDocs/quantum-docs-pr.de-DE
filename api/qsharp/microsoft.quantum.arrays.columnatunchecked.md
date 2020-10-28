---
uid: Microsoft.Quantum.Arrays.ColumnAtUnchecked
title: Columnatdeaktiviert-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: ColumnAtUnchecked
qsharp.summary: This function does not check for matrix shape
ms.openlocfilehash: 17211c1ae1fe12fcadf34a9411f9b0cf0cdcab50
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706162"
---
# <a name="columnatunchecked-function"></a><span data-ttu-id="a6d60-102">Columnatdeaktiviert-Funktion</span><span class="sxs-lookup"><span data-stu-id="a6d60-102">ColumnAtUnchecked function</span></span>

<span data-ttu-id="a6d60-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="a6d60-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="a6d60-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="a6d60-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="a6d60-105">Diese Funktion prüft nicht die Form "Matrix".</span><span class="sxs-lookup"><span data-stu-id="a6d60-105">This function does not check for matrix shape</span></span>

```qsharp
function ColumnAtUnchecked<'T> (column : Int, matrix : 'T[][]) : 'T[]
```


## <a name="description"></a><span data-ttu-id="a6d60-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a6d60-106">Description</span></span>

<span data-ttu-id="a6d60-107">Diese Funktion kann in anderen mehrdimensionalen Funktionen verwendet werden, die die Eingabe Matrix bereits auf eine gültige rechteckige Form überprüft haben.</span><span class="sxs-lookup"><span data-stu-id="a6d60-107">This function can be used in other multidimensional functions, which already check the input matrix for a valid rectangular shape.</span></span>

## <a name="input"></a><span data-ttu-id="a6d60-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a6d60-108">Input</span></span>

### <a name="column--int"></a><span data-ttu-id="a6d60-109">Spalte: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="a6d60-109">column : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>




### <a name="matrix--t"></a><span data-ttu-id="a6d60-110">Matrix: 't [] []</span><span class="sxs-lookup"><span data-stu-id="a6d60-110">matrix : 'T[][]</span></span>





## <a name="output--t"></a><span data-ttu-id="a6d60-111">Ausgabe: 't []</span><span class="sxs-lookup"><span data-stu-id="a6d60-111">Output : 'T[]</span></span>



## <a name="type-parameters"></a><span data-ttu-id="a6d60-112">Typparameter</span><span class="sxs-lookup"><span data-stu-id="a6d60-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="a6d60-113">GIF</span><span class="sxs-lookup"><span data-stu-id="a6d60-113">'T</span></span>

