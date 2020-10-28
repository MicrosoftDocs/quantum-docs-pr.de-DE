---
uid: Microsoft.Quantum.Core.RangeReverse
title: Rangereverse-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Core
qsharp.name: RangeReverse
qsharp.summary: Returns a new range which is the reverse of the input range.
ms.openlocfilehash: d4e612d2f175015b7193634aeec12f9df12df7d3
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702864"
---
# <a name="rangereverse-function"></a><span data-ttu-id="a78e2-102">Rangereverse-Funktion</span><span class="sxs-lookup"><span data-stu-id="a78e2-102">RangeReverse function</span></span>

<span data-ttu-id="a78e2-103">Namespace: [Microsoft. Quantum. Core](xref:Microsoft.Quantum.Core)</span><span class="sxs-lookup"><span data-stu-id="a78e2-103">Namespace: [Microsoft.Quantum.Core](xref:Microsoft.Quantum.Core)</span></span>

<span data-ttu-id="a78e2-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="a78e2-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="a78e2-105">Gibt einen neuen Bereich zurück, bei dem es sich um den umgekehrten Bereich des Eingabe Bereichs handelt.</span><span class="sxs-lookup"><span data-stu-id="a78e2-105">Returns a new range which is the reverse of the input range.</span></span>

```qsharp
function RangeReverse (r : Range) : Range
```


## <a name="input"></a><span data-ttu-id="a78e2-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a78e2-106">Input</span></span>

### <a name="r--range"></a><span data-ttu-id="a78e2-107">r: [Bereich](xref:microsoft.quantum.lang-ref.range)</span><span class="sxs-lookup"><span data-stu-id="a78e2-107">r : [Range](xref:microsoft.quantum.lang-ref.range)</span></span>

<span data-ttu-id="a78e2-108">Eingabebereich.</span><span class="sxs-lookup"><span data-stu-id="a78e2-108">Input range.</span></span>



## <a name="output--range"></a><span data-ttu-id="a78e2-109">Ausgabe: [Bereich](xref:microsoft.quantum.lang-ref.range)</span><span class="sxs-lookup"><span data-stu-id="a78e2-109">Output : [Range](xref:microsoft.quantum.lang-ref.range)</span></span>

<span data-ttu-id="a78e2-110">Ein neuer Bereich, der das Gegenteil des angegebenen Bereichs ist.</span><span class="sxs-lookup"><span data-stu-id="a78e2-110">A new range that is the reverse of the given range.</span></span>

## <a name="remarks"></a><span data-ttu-id="a78e2-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a78e2-111">Remarks</span></span>

<span data-ttu-id="a78e2-112">Beachten Sie, dass der umgekehrte Bereich eines Bereichs nicht einfach " `end` .. `-step` .." ist `start` , da das tatsächliche letzte Element eines Bereichs möglicherweise nicht mit identisch `end` ist.</span><span class="sxs-lookup"><span data-stu-id="a78e2-112">Note that the reverse of a range is not simply `end`..`-step`..`start`, because the actual last element of a range may not be the same as `end`.</span></span>