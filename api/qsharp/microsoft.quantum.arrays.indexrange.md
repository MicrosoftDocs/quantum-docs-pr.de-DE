---
uid: Microsoft.Quantum.Arrays.IndexRange
title: Indexrange-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: IndexRange
qsharp.summary: Given an array, returns a range over the indices of that array, suitable for use in a for loop.
ms.openlocfilehash: 5afd4cc260ac3e384d2736bf7b43d941afd9ef73
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220942"
---
# <a name="indexrange-function"></a><span data-ttu-id="1b27e-102">Indexrange-Funktion</span><span class="sxs-lookup"><span data-stu-id="1b27e-102">IndexRange function</span></span>

<span data-ttu-id="1b27e-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="1b27e-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="1b27e-104">Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="1b27e-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="1b27e-105">Gibt bei Angabe eines Arrays einen Bereich über die Indizes dieses Arrays zurück, der für die Verwendung in einer for-Schleife geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="1b27e-105">Given an array, returns a range over the indices of that array, suitable for use in a for loop.</span></span>

```qsharp
function IndexRange<'TElement> (array : 'TElement[]) : Range
```


## <a name="input"></a><span data-ttu-id="1b27e-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="1b27e-106">Input</span></span>

### <a name="array--telement"></a><span data-ttu-id="1b27e-107">Array: ' telements []</span><span class="sxs-lookup"><span data-stu-id="1b27e-107">array : 'TElement[]</span></span>

<span data-ttu-id="1b27e-108">Ein Array, für das ein Bereich von Indizes zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="1b27e-108">An array for which a range of indices should be returned.</span></span>



## <a name="output--range"></a><span data-ttu-id="1b27e-109">Ausgabe: [Bereich](xref:microsoft.quantum.lang-ref.range)</span><span class="sxs-lookup"><span data-stu-id="1b27e-109">Output : [Range](xref:microsoft.quantum.lang-ref.range)</span></span>

<span data-ttu-id="1b27e-110">Ein Bereich über alle Indizes des Arrays.</span><span class="sxs-lookup"><span data-stu-id="1b27e-110">A range over all indices of the array.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="1b27e-111">Typparameter</span><span class="sxs-lookup"><span data-stu-id="1b27e-111">Type Parameters</span></span>

### <a name="telement"></a><span data-ttu-id="1b27e-112">' Telements '</span><span class="sxs-lookup"><span data-stu-id="1b27e-112">'TElement</span></span>

<span data-ttu-id="1b27e-113">Der Typ der Elemente des Arrays.</span><span class="sxs-lookup"><span data-stu-id="1b27e-113">The type of elements of the array.</span></span>