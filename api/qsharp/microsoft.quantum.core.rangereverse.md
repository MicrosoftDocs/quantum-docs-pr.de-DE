---
uid: Microsoft.Quantum.Core.RangeReverse
title: Rangereverse-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Core
qsharp.name: RangeReverse
qsharp.summary: Returns a new range which is the reverse of the input range.
ms.openlocfilehash: f3b94d3c6fa6350a2c337f8bc8d889d24d87a85b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853656"
---
# <a name="rangereverse-function"></a><span data-ttu-id="ee71c-102">Rangereverse-Funktion</span><span class="sxs-lookup"><span data-stu-id="ee71c-102">RangeReverse function</span></span>

<span data-ttu-id="ee71c-103">Namespace: [Microsoft. Quantum. Core](xref:Microsoft.Quantum.Core)</span><span class="sxs-lookup"><span data-stu-id="ee71c-103">Namespace: [Microsoft.Quantum.Core](xref:Microsoft.Quantum.Core)</span></span>

<span data-ttu-id="ee71c-104">Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="ee71c-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="ee71c-105">Gibt einen neuen Bereich zurück, bei dem es sich um den umgekehrten Bereich des Eingabe Bereichs handelt.</span><span class="sxs-lookup"><span data-stu-id="ee71c-105">Returns a new range which is the reverse of the input range.</span></span>

```qsharp
function RangeReverse (r : Range) : Range
```


## <a name="input"></a><span data-ttu-id="ee71c-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ee71c-106">Input</span></span>

### <a name="r--range"></a><span data-ttu-id="ee71c-107">r: [Bereich](xref:microsoft.quantum.lang-ref.range)</span><span class="sxs-lookup"><span data-stu-id="ee71c-107">r : [Range](xref:microsoft.quantum.lang-ref.range)</span></span>

<span data-ttu-id="ee71c-108">Eingabebereich.</span><span class="sxs-lookup"><span data-stu-id="ee71c-108">Input range.</span></span>



## <a name="output--range"></a><span data-ttu-id="ee71c-109">Ausgabe: [Bereich](xref:microsoft.quantum.lang-ref.range)</span><span class="sxs-lookup"><span data-stu-id="ee71c-109">Output : [Range](xref:microsoft.quantum.lang-ref.range)</span></span>

<span data-ttu-id="ee71c-110">Ein neuer Bereich, der das Gegenteil des angegebenen Bereichs ist.</span><span class="sxs-lookup"><span data-stu-id="ee71c-110">A new range that is the reverse of the given range.</span></span>

## <a name="remarks"></a><span data-ttu-id="ee71c-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ee71c-111">Remarks</span></span>

<span data-ttu-id="ee71c-112">Beachten Sie, dass der umgekehrte Bereich eines Bereichs nicht einfach " `end` .. `-step` .." ist `start` , da das tatsächliche letzte Element eines Bereichs möglicherweise nicht mit identisch `end` ist.</span><span class="sxs-lookup"><span data-stu-id="ee71c-112">Note that the reverse of a range is not simply `end`..`-step`..`start`, because the actual last element of a range may not be the same as `end`.</span></span>