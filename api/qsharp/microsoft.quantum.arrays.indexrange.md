---
uid: Microsoft.Quantum.Arrays.IndexRange
title: Indexrange-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: IndexRange
qsharp.summary: Given an array, returns a range over the indices of that array, suitable for use in a for loop.
ms.openlocfilehash: 7f9779acd4a781c50388217aa780710bd0b99ff3
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705962"
---
# <a name="indexrange-function"></a><span data-ttu-id="2e65a-102">Indexrange-Funktion</span><span class="sxs-lookup"><span data-stu-id="2e65a-102">IndexRange function</span></span>

<span data-ttu-id="2e65a-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="2e65a-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="2e65a-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="2e65a-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="2e65a-105">Gibt bei Angabe eines Arrays einen Bereich über die Indizes dieses Arrays zurück, der für die Verwendung in einer for-Schleife geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="2e65a-105">Given an array, returns a range over the indices of that array, suitable for use in a for loop.</span></span>

```qsharp
function IndexRange<'TElement> (array : 'TElement[]) : Range
```


## <a name="input"></a><span data-ttu-id="2e65a-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2e65a-106">Input</span></span>

### <a name="array--telement"></a><span data-ttu-id="2e65a-107">Array: ' telements []</span><span class="sxs-lookup"><span data-stu-id="2e65a-107">array : 'TElement[]</span></span>

<span data-ttu-id="2e65a-108">Ein Array, für das ein Bereich von Indizes zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="2e65a-108">An array for which a range of indices should be returned.</span></span>



## <a name="output--range"></a><span data-ttu-id="2e65a-109">Ausgabe: [Bereich](xref:microsoft.quantum.lang-ref.range)</span><span class="sxs-lookup"><span data-stu-id="2e65a-109">Output : [Range](xref:microsoft.quantum.lang-ref.range)</span></span>

<span data-ttu-id="2e65a-110">Ein Bereich über alle Indizes des Arrays.</span><span class="sxs-lookup"><span data-stu-id="2e65a-110">A range over all indices of the array.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="2e65a-111">Typparameter</span><span class="sxs-lookup"><span data-stu-id="2e65a-111">Type Parameters</span></span>

### <a name="telement"></a><span data-ttu-id="2e65a-112">' Telements '</span><span class="sxs-lookup"><span data-stu-id="2e65a-112">'TElement</span></span>

<span data-ttu-id="2e65a-113">Der Typ der Elemente des Arrays.</span><span class="sxs-lookup"><span data-stu-id="2e65a-113">The type of elements of the array.</span></span>