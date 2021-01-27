---
uid: Microsoft.Quantum.Preparation.ApproximatelyUnprepareArbitraryStatePlan
title: Ungefäatelyunpreparearbitrarystateplan-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: ApproximatelyUnprepareArbitraryStatePlan
qsharp.summary: Implementation step of arbitrary state preparation procedure.
ms.openlocfilehash: d506e3a8bff365f1c99d4ed1eb41d29ba3dbeb18
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842437"
---
# <a name="approximatelyunpreparearbitrarystateplan-function"></a><span data-ttu-id="ce786-102">Ungefäatelyunpreparearbitrarystateplan-Funktion</span><span class="sxs-lookup"><span data-stu-id="ce786-102">ApproximatelyUnprepareArbitraryStatePlan function</span></span>

<span data-ttu-id="ce786-103">Namespace: [Microsoft. Quantum. Preparation](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="ce786-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="ce786-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="ce786-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="ce786-105">Implementierungs Schritt eines willkürlichen Zustands Vorbereitungs Verfahrens.</span><span class="sxs-lookup"><span data-stu-id="ce786-105">Implementation step of arbitrary state preparation procedure.</span></span>

```qsharp
function ApproximatelyUnprepareArbitraryStatePlan (tolerance : Double, coefficients : Microsoft.Quantum.Math.ComplexPolar[], (rngControl : Range, idxTarget : Int)) : (Qubit[] => Unit is Adj + Ctl)[]
```


## <a name="input"></a><span data-ttu-id="ce786-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ce786-106">Input</span></span>

### <a name="tolerance--double"></a><span data-ttu-id="ce786-107">Toleranz: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="ce786-107">tolerance : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>




### <a name="coefficients--complexpolar"></a><span data-ttu-id="ce786-108">Koeffizienten: [complexpolar](xref:Microsoft.Quantum.Math.ComplexPolar)[]</span><span class="sxs-lookup"><span data-stu-id="ce786-108">coefficients : [ComplexPolar](xref:Microsoft.Quantum.Math.ComplexPolar)[]</span></span>




### <a name="rngcontrol--range"></a><span data-ttu-id="ce786-109">rngcontrol: [Bereich](xref:microsoft.quantum.lang-ref.range)</span><span class="sxs-lookup"><span data-stu-id="ce786-109">rngControl : [Range](xref:microsoft.quantum.lang-ref.range)</span></span>




### <a name="idxtarget--int"></a><span data-ttu-id="ce786-110">idxtarget: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="ce786-110">idxTarget : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>





## <a name="output--qubit--unit--is-adj--ctl"></a><span data-ttu-id="ce786-111">Ausgabe: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL []</span><span class="sxs-lookup"><span data-stu-id="ce786-111">Output : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl[]</span></span>



## <a name="see-also"></a><span data-ttu-id="ce786-112">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ce786-112">See Also</span></span>

- [<span data-ttu-id="ce786-113">Microsoft. Quantum. Preparation. preparearbitrarystate</span><span class="sxs-lookup"><span data-stu-id="ce786-113">Microsoft.Quantum.Preparation.PrepareArbitraryState</span></span>](xref:Microsoft.Quantum.Preparation.PrepareArbitraryState)
- [<span data-ttu-id="ce786-114">Microsoft. Quantum. Canon. multiplexpauli</span><span class="sxs-lookup"><span data-stu-id="ce786-114">Microsoft.Quantum.Canon.MultiplexPauli</span></span>](xref:Microsoft.Quantum.Canon.MultiplexPauli)