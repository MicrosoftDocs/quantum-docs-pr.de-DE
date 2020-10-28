---
uid: Microsoft.Quantum.Diagnostics.AssertAllZeroWithinTolerance
title: Assertallzerowithintoleranz-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertAllZeroWithinTolerance
qsharp.summary: Assert that given qubits are all in $\ket{0}$ state up to a given tolerance.
ms.openlocfilehash: 5e401904086323fabef7914d34463f50e4c38862
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702785"
---
# <a name="assertallzerowithintolerance-operation"></a><span data-ttu-id="80f2e-102">Assertallzerowithintoleranz-Vorgang</span><span class="sxs-lookup"><span data-stu-id="80f2e-102">AssertAllZeroWithinTolerance operation</span></span>

<span data-ttu-id="80f2e-103">Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="80f2e-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="80f2e-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="80f2e-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="80f2e-105">Bestätigen Sie, dass die angegebenen Qubits alle in $ \ket {0} $ State bis zu einer gegebenen Toleranz aufweisen.</span><span class="sxs-lookup"><span data-stu-id="80f2e-105">Assert that given qubits are all in $\ket{0}$ state up to a given tolerance.</span></span>

```qsharp
operation AssertAllZeroWithinTolerance (qubits : Qubit[], tolerance : Double) : Unit
```


## <a name="input"></a><span data-ttu-id="80f2e-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="80f2e-106">Input</span></span>

### <a name="qubits--qubit"></a><span data-ttu-id="80f2e-107">Qubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="80f2e-107">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="80f2e-108">Qubits, die in $ \ket {0} $ State übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="80f2e-108">Qubits that are asserted to be in $\ket{0}$ state.</span></span>


### <a name="tolerance--double"></a><span data-ttu-id="80f2e-109">Toleranz: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="80f2e-109">tolerance : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="80f2e-110">Die Genauigkeit, mit der sich der Status in "$ \ket $ State" befinden sollte. {0}</span><span class="sxs-lookup"><span data-stu-id="80f2e-110">Accuracy with which the state should be in $\ket{0}$ state</span></span>



## <a name="output--unit"></a><span data-ttu-id="80f2e-111">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="80f2e-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="80f2e-112">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="80f2e-112">See Also</span></span>

- [<span data-ttu-id="80f2e-113">Microsoft. Quantum. Diagnostics. assertqubitwithintoleranz</span><span class="sxs-lookup"><span data-stu-id="80f2e-113">Microsoft.Quantum.Diagnostics.AssertQubitWithinTolerance</span></span>](xref:Microsoft.Quantum.Diagnostics.AssertQubitWithinTolerance)