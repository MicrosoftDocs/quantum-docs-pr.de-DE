---
uid: Microsoft.Quantum.Diagnostics.AssertQubitWithinTolerance
title: Assertqubitwithintoleranz-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertQubitWithinTolerance
qsharp.summary: Asserts that the qubit `q` is in the expected eigenstate of the Pauli Z operator up to a given tolerance.
ms.openlocfilehash: 3fe4aa739c5e15199401aecb76ef551e52f6dcff
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702714"
---
# <a name="assertqubitwithintolerance-operation"></a><span data-ttu-id="c3e01-102">Assertqubitwithintoleranz-Vorgang</span><span class="sxs-lookup"><span data-stu-id="c3e01-102">AssertQubitWithinTolerance operation</span></span>

<span data-ttu-id="c3e01-103">Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="c3e01-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="c3e01-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="c3e01-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="c3e01-105">Bestätigt, dass das Qubit den `q` erwarteten Zustand des Pauli Z-Operators bis zu einer gegebenen Toleranz aufweist.</span><span class="sxs-lookup"><span data-stu-id="c3e01-105">Asserts that the qubit `q` is in the expected eigenstate of the Pauli Z operator up to a given tolerance.</span></span>

```qsharp
operation AssertQubitWithinTolerance (expected : Result, q : Qubit, tolerance : Double) : Unit
```


## <a name="input"></a><span data-ttu-id="c3e01-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c3e01-106">Input</span></span>

### <a name="expected--__invalidresult__"></a><span data-ttu-id="c3e01-107">erwartet: __ungültig <Result>__</span><span class="sxs-lookup"><span data-stu-id="c3e01-107">expected : __invalid<Result>__</span></span>

<span data-ttu-id="c3e01-108">Der Zustand, in dem das Qubit erwartet wird: `Zero` oder `One` .</span><span class="sxs-lookup"><span data-stu-id="c3e01-108">Which state the qubit is expected to be in: `Zero` or `One`.</span></span>


### <a name="q--qubit"></a><span data-ttu-id="c3e01-109">q: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="c3e01-109">q : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="c3e01-110">Das Qubit, dessen Zustand bestätigt wird.</span><span class="sxs-lookup"><span data-stu-id="c3e01-110">The qubit whose state is asserted.</span></span>


### <a name="tolerance--double"></a><span data-ttu-id="c3e01-111">Toleranz: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="c3e01-111">tolerance : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="c3e01-112">Toleranz für die Wahrscheinlichkeit einer Messung des Qubit, das das erwartete Ergebnis zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="c3e01-112">Tolerance on the probability of a measurement of the qubit returning the expected result.</span></span>



## <a name="output--unit"></a><span data-ttu-id="c3e01-113">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="c3e01-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="c3e01-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c3e01-114">Remarks</span></span>

<span data-ttu-id="c3e01-115"><xref:microsoft.quantum.diagnostics.assertqubitisinstatewithintolerance> ermöglicht das Assert von willkürlichen Qubit-Zuständen anstelle von $Z $ eigen Zuständen.</span><span class="sxs-lookup"><span data-stu-id="c3e01-115"><xref:microsoft.quantum.diagnostics.assertqubitisinstatewithintolerance> allows for asserting arbitrary qubit states rather than only $Z$ eigenstates.</span></span>

## <a name="see-also"></a><span data-ttu-id="c3e01-116">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c3e01-116">See Also</span></span>

- [<span data-ttu-id="c3e01-117">Microsoft. Quantum. Diagnostics. assertqubitisinstatewithintoleranz</span><span class="sxs-lookup"><span data-stu-id="c3e01-117">Microsoft.Quantum.Diagnostics.AssertQubitIsInStateWithinTolerance</span></span>](xref:Microsoft.Quantum.Diagnostics.AssertQubitIsInStateWithinTolerance)