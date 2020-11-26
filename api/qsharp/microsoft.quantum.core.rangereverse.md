---
uid: Microsoft.Quantum.Core.RangeReverse
title: Rangereverse-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Core
qsharp.name: RangeReverse
qsharp.summary: Returns a new range which is the reverse of the input range.
ms.openlocfilehash: 7bd7c55abe0b56b9d30b4c6e91f7175101dd2948
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96213836"
---
# <a name="rangereverse-function"></a><span data-ttu-id="04508-102">Rangereverse-Funktion</span><span class="sxs-lookup"><span data-stu-id="04508-102">RangeReverse function</span></span>

<span data-ttu-id="04508-103">Namespace: [Microsoft. Quantum. Core](xref:Microsoft.Quantum.Core)</span><span class="sxs-lookup"><span data-stu-id="04508-103">Namespace: [Microsoft.Quantum.Core](xref:Microsoft.Quantum.Core)</span></span>

<span data-ttu-id="04508-104">Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="04508-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="04508-105">Gibt einen neuen Bereich zurück, bei dem es sich um den umgekehrten Bereich des Eingabe Bereichs handelt.</span><span class="sxs-lookup"><span data-stu-id="04508-105">Returns a new range which is the reverse of the input range.</span></span>

```qsharp
function RangeReverse (r : Range) : Range
```


## <a name="input"></a><span data-ttu-id="04508-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="04508-106">Input</span></span>

### <a name="r--range"></a><span data-ttu-id="04508-107">r: [Bereich](xref:microsoft.quantum.lang-ref.range)</span><span class="sxs-lookup"><span data-stu-id="04508-107">r : [Range](xref:microsoft.quantum.lang-ref.range)</span></span>

<span data-ttu-id="04508-108">Eingabebereich.</span><span class="sxs-lookup"><span data-stu-id="04508-108">Input range.</span></span>



## <a name="output--range"></a><span data-ttu-id="04508-109">Ausgabe: [Bereich](xref:microsoft.quantum.lang-ref.range)</span><span class="sxs-lookup"><span data-stu-id="04508-109">Output : [Range](xref:microsoft.quantum.lang-ref.range)</span></span>

<span data-ttu-id="04508-110">Ein neuer Bereich, der das Gegenteil des angegebenen Bereichs ist.</span><span class="sxs-lookup"><span data-stu-id="04508-110">A new range that is the reverse of the given range.</span></span>

## <a name="remarks"></a><span data-ttu-id="04508-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="04508-111">Remarks</span></span>

<span data-ttu-id="04508-112">Beachten Sie, dass der umgekehrte Bereich eines Bereichs nicht einfach " `end` .. `-step` .." ist `start` , da das tatsächliche letzte Element eines Bereichs möglicherweise nicht mit identisch `end` ist.</span><span class="sxs-lookup"><span data-stu-id="04508-112">Note that the reverse of a range is not simply `end`..`-step`..`start`, because the actual last element of a range may not be the same as `end`.</span></span>