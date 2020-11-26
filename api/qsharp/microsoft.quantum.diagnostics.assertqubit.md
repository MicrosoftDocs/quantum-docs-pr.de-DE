---
uid: Microsoft.Quantum.Diagnostics.AssertQubit
title: Assertqubit-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertQubit
qsharp.summary: Asserts that the qubit `q` is in the expected eigenstate of the Pauli Z operator.
ms.openlocfilehash: 0e005230427bbd570133712679c51661e7ae6496
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96202242"
---
# <a name="assertqubit-operation"></a><span data-ttu-id="72424-102">Assertqubit-Vorgang</span><span class="sxs-lookup"><span data-stu-id="72424-102">AssertQubit operation</span></span>

<span data-ttu-id="72424-103">Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="72424-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="72424-104">Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="72424-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="72424-105">Bestätigt, dass sich das Qubit `q` im erwarteten eigen Zustand des Pauli Z-Operators befindet.</span><span class="sxs-lookup"><span data-stu-id="72424-105">Asserts that the qubit `q` is in the expected eigenstate of the Pauli Z operator.</span></span>

```qsharp
operation AssertQubit (expected : Result, q : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="72424-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="72424-106">Input</span></span>

### <a name="expected--__invalidresult__"></a><span data-ttu-id="72424-107">erwartet: __ungültig <Result>__</span><span class="sxs-lookup"><span data-stu-id="72424-107">expected : __invalid<Result>__</span></span>

<span data-ttu-id="72424-108">Der Zustand, in dem das Qubit erwartet wird: `Zero` oder `One` .</span><span class="sxs-lookup"><span data-stu-id="72424-108">Which state the qubit is expected to be in: `Zero` or `One`.</span></span>


### <a name="q--qubit"></a><span data-ttu-id="72424-109">q: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="72424-109">q : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="72424-110">Das Qubit, dessen Zustand bestätigt wird.</span><span class="sxs-lookup"><span data-stu-id="72424-110">The qubit whose state is asserted.</span></span>



## <a name="output--unit"></a><span data-ttu-id="72424-111">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="72424-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="72424-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="72424-112">Remarks</span></span>

<span data-ttu-id="72424-113"><xref:microsoft.quantum.diagnostics.assertqubitisinstatewithintolerance> ermöglicht das Assert von willkürlichen Qubit-Zuständen anstelle von $Z $ eigen Zuständen.</span><span class="sxs-lookup"><span data-stu-id="72424-113"><xref:microsoft.quantum.diagnostics.assertqubitisinstatewithintolerance> allows for asserting arbitrary qubit states rather than only $Z$ eigenstates.</span></span>

## <a name="see-also"></a><span data-ttu-id="72424-114">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="72424-114">See Also</span></span>

- [<span data-ttu-id="72424-115">Microsoft. Quantum. Diagnostics. assertqubitisinstatewithintoleranz</span><span class="sxs-lookup"><span data-stu-id="72424-115">Microsoft.Quantum.Diagnostics.AssertQubitIsInStateWithinTolerance</span></span>](xref:Microsoft.Quantum.Diagnostics.AssertQubitIsInStateWithinTolerance)