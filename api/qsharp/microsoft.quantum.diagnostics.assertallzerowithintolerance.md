---
uid: Microsoft.Quantum.Diagnostics.AssertAllZeroWithinTolerance
title: Assertallzerowithintoleranz-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertAllZeroWithinTolerance
qsharp.summary: Assert that given qubits are all in $\ket{0}$ state up to a given tolerance.
ms.openlocfilehash: a2e73bbc8949b3cdb7733cfc8aae35680e54d2cf
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96202480"
---
# <a name="assertallzerowithintolerance-operation"></a><span data-ttu-id="9eff1-102">Assertallzerowithintoleranz-Vorgang</span><span class="sxs-lookup"><span data-stu-id="9eff1-102">AssertAllZeroWithinTolerance operation</span></span>

<span data-ttu-id="9eff1-103">Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="9eff1-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="9eff1-104">Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="9eff1-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="9eff1-105">Bestätigen Sie, dass die angegebenen Qubits alle in $ \ket {0} $ State bis zu einer gegebenen Toleranz aufweisen.</span><span class="sxs-lookup"><span data-stu-id="9eff1-105">Assert that given qubits are all in $\ket{0}$ state up to a given tolerance.</span></span>

```qsharp
operation AssertAllZeroWithinTolerance (qubits : Qubit[], tolerance : Double) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="9eff1-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="9eff1-106">Input</span></span>

### <a name="qubits--qubit"></a><span data-ttu-id="9eff1-107">Qubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="9eff1-107">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="9eff1-108">Qubits, die in $ \ket {0} $ State übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="9eff1-108">Qubits that are asserted to be in $\ket{0}$ state.</span></span>


### <a name="tolerance--double"></a><span data-ttu-id="9eff1-109">Toleranz: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="9eff1-109">tolerance : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="9eff1-110">Die Genauigkeit, mit der sich der Status in "$ \ket $ State" befinden sollte. {0}</span><span class="sxs-lookup"><span data-stu-id="9eff1-110">Accuracy with which the state should be in $\ket{0}$ state</span></span>



## <a name="output--unit"></a><span data-ttu-id="9eff1-111">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="9eff1-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="9eff1-112">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="9eff1-112">See Also</span></span>

- [<span data-ttu-id="9eff1-113">Microsoft. Quantum. Diagnostics. assertqubitwithintoleranz</span><span class="sxs-lookup"><span data-stu-id="9eff1-113">Microsoft.Quantum.Diagnostics.AssertQubitWithinTolerance</span></span>](xref:Microsoft.Quantum.Diagnostics.AssertQubitWithinTolerance)