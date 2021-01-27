---
uid: Microsoft.Quantum.Arrays.IndexRange
title: Indexrange-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: IndexRange
qsharp.summary: Given an array, returns a range over the indices of that array, suitable for use in a for loop.
ms.openlocfilehash: 043b56a1ac3cbe5cd59cdd45d3725f301d81a6ee
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845780"
---
# <a name="indexrange-function"></a><span data-ttu-id="23e66-102">Indexrange-Funktion</span><span class="sxs-lookup"><span data-stu-id="23e66-102">IndexRange function</span></span>

<span data-ttu-id="23e66-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="23e66-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="23e66-104">Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="23e66-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="23e66-105">Gibt bei Angabe eines Arrays einen Bereich über die Indizes dieses Arrays zurück, der für die Verwendung in einer for-Schleife geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="23e66-105">Given an array, returns a range over the indices of that array, suitable for use in a for loop.</span></span>

```qsharp
function IndexRange<'TElement> (array : 'TElement[]) : Range
```


## <a name="input"></a><span data-ttu-id="23e66-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="23e66-106">Input</span></span>

### <a name="array--telement"></a><span data-ttu-id="23e66-107">Array: ' telements []</span><span class="sxs-lookup"><span data-stu-id="23e66-107">array : 'TElement[]</span></span>

<span data-ttu-id="23e66-108">Ein Array, für das ein Bereich von Indizes zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="23e66-108">An array for which a range of indices should be returned.</span></span>



## <a name="output--range"></a><span data-ttu-id="23e66-109">Ausgabe: [Bereich](xref:microsoft.quantum.lang-ref.range)</span><span class="sxs-lookup"><span data-stu-id="23e66-109">Output : [Range](xref:microsoft.quantum.lang-ref.range)</span></span>

<span data-ttu-id="23e66-110">Ein Bereich über alle Indizes des Arrays.</span><span class="sxs-lookup"><span data-stu-id="23e66-110">A range over all indices of the array.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="23e66-111">Typparameter</span><span class="sxs-lookup"><span data-stu-id="23e66-111">Type Parameters</span></span>

### <a name="telement"></a><span data-ttu-id="23e66-112">' Telements '</span><span class="sxs-lookup"><span data-stu-id="23e66-112">'TElement</span></span>

<span data-ttu-id="23e66-113">Der Typ der Elemente des Arrays.</span><span class="sxs-lookup"><span data-stu-id="23e66-113">The type of elements of the array.</span></span>

## <a name="example"></a><span data-ttu-id="23e66-114">Beispiel</span><span class="sxs-lookup"><span data-stu-id="23e66-114">Example</span></span>

<span data-ttu-id="23e66-115">Die folgenden `for` Schleifen sind äquivalent:</span><span class="sxs-lookup"><span data-stu-id="23e66-115">The following `for` loops are equivalent:</span></span>

```qsharp
for (idx in IndexRange(array)) { ... }
for (idx in IndexRange(array)) { ... }
```