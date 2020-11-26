---
uid: Microsoft.Quantum.Arrays.ColumnAtUnchecked
title: Columnatdeaktiviert-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: ColumnAtUnchecked
qsharp.summary: This function does not check for matrix shape
ms.openlocfilehash: 06fce23bbf7142ee0e0b0ed3f2c0578676f2097b
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96221588"
---
# <a name="columnatunchecked-function"></a><span data-ttu-id="e3668-102">Columnatdeaktiviert-Funktion</span><span class="sxs-lookup"><span data-stu-id="e3668-102">ColumnAtUnchecked function</span></span>

<span data-ttu-id="e3668-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="e3668-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="e3668-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="e3668-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="e3668-105">Diese Funktion prüft nicht die Form "Matrix".</span><span class="sxs-lookup"><span data-stu-id="e3668-105">This function does not check for matrix shape</span></span>

```qsharp
function ColumnAtUnchecked<'T> (column : Int, matrix : 'T[][]) : 'T[]
```


## <a name="description"></a><span data-ttu-id="e3668-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e3668-106">Description</span></span>

<span data-ttu-id="e3668-107">Diese Funktion kann in anderen mehrdimensionalen Funktionen verwendet werden, die die Eingabe Matrix bereits auf eine gültige rechteckige Form überprüft haben.</span><span class="sxs-lookup"><span data-stu-id="e3668-107">This function can be used in other multidimensional functions, which already check the input matrix for a valid rectangular shape.</span></span>

## <a name="input"></a><span data-ttu-id="e3668-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e3668-108">Input</span></span>

### <a name="column--int"></a><span data-ttu-id="e3668-109">Spalte: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="e3668-109">column : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>




### <a name="matrix--t"></a><span data-ttu-id="e3668-110">Matrix: 't [] []</span><span class="sxs-lookup"><span data-stu-id="e3668-110">matrix : 'T[][]</span></span>





## <a name="output--t"></a><span data-ttu-id="e3668-111">Ausgabe: 't []</span><span class="sxs-lookup"><span data-stu-id="e3668-111">Output : 'T[]</span></span>



## <a name="type-parameters"></a><span data-ttu-id="e3668-112">Typparameter</span><span class="sxs-lookup"><span data-stu-id="e3668-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="e3668-113">GIF</span><span class="sxs-lookup"><span data-stu-id="e3668-113">'T</span></span>

