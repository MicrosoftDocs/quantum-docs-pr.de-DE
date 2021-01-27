---
uid: Microsoft.Quantum.Diagnostics.AssertQubitWithinTolerance
title: Assertqubitwithintoleranz-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertQubitWithinTolerance
qsharp.summary: Asserts that the qubit `q` is in the expected eigenstate of the Pauli Z operator up to a given tolerance.
ms.openlocfilehash: 7f57fc7a29d3eb86dc94cb24230d52b37eb6971d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853436"
---
# <a name="assertqubitwithintolerance-operation"></a><span data-ttu-id="f7661-102">Assertqubitwithintoleranz-Vorgang</span><span class="sxs-lookup"><span data-stu-id="f7661-102">AssertQubitWithinTolerance operation</span></span>

<span data-ttu-id="f7661-103">Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="f7661-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="f7661-104">Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="f7661-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="f7661-105">Bestätigt, dass das Qubit den `q` erwarteten Zustand des Pauli Z-Operators bis zu einer gegebenen Toleranz aufweist.</span><span class="sxs-lookup"><span data-stu-id="f7661-105">Asserts that the qubit `q` is in the expected eigenstate of the Pauli Z operator up to a given tolerance.</span></span>

```qsharp
operation AssertQubitWithinTolerance (expected : Result, q : Qubit, tolerance : Double) : Unit
```


## <a name="input"></a><span data-ttu-id="f7661-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f7661-106">Input</span></span>

### <a name="expected--__invalidresult__"></a><span data-ttu-id="f7661-107">erwartet: __ungültig <Result>__</span><span class="sxs-lookup"><span data-stu-id="f7661-107">expected : __invalid<Result>__</span></span>

<span data-ttu-id="f7661-108">Der Zustand, in dem das Qubit erwartet wird: `Zero` oder `One` .</span><span class="sxs-lookup"><span data-stu-id="f7661-108">Which state the qubit is expected to be in: `Zero` or `One`.</span></span>


### <a name="q--qubit"></a><span data-ttu-id="f7661-109">q: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="f7661-109">q : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="f7661-110">Das Qubit, dessen Zustand bestätigt wird.</span><span class="sxs-lookup"><span data-stu-id="f7661-110">The qubit whose state is asserted.</span></span>


### <a name="tolerance--double"></a><span data-ttu-id="f7661-111">Toleranz: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="f7661-111">tolerance : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="f7661-112">Toleranz für die Wahrscheinlichkeit einer Messung des Qubit, das das erwartete Ergebnis zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="f7661-112">Tolerance on the probability of a measurement of the qubit returning the expected result.</span></span>



## <a name="output--unit"></a><span data-ttu-id="f7661-113">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="f7661-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="f7661-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f7661-114">Remarks</span></span>

<span data-ttu-id="f7661-115"><xref:microsoft.quantum.diagnostics.assertqubitisinstatewithintolerance> ermöglicht das Assert von willkürlichen Qubit-Zuständen anstelle von $Z $ eigen Zuständen.</span><span class="sxs-lookup"><span data-stu-id="f7661-115"><xref:microsoft.quantum.diagnostics.assertqubitisinstatewithintolerance> allows for asserting arbitrary qubit states rather than only $Z$ eigenstates.</span></span>

## <a name="see-also"></a><span data-ttu-id="f7661-116">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="f7661-116">See Also</span></span>

- [<span data-ttu-id="f7661-117">Microsoft. Quantum. Diagnostics. assertqubitisinstatewithintoleranz</span><span class="sxs-lookup"><span data-stu-id="f7661-117">Microsoft.Quantum.Diagnostics.AssertQubitIsInStateWithinTolerance</span></span>](xref:Microsoft.Quantum.Diagnostics.AssertQubitIsInStateWithinTolerance)