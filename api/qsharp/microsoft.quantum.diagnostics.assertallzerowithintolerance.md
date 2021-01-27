---
uid: Microsoft.Quantum.Diagnostics.AssertAllZeroWithinTolerance
title: Assertallzerowithintoleranz-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertAllZeroWithinTolerance
qsharp.summary: Assert that given qubits are all in $\ket{0}$ state up to a given tolerance.
ms.openlocfilehash: 281855ec79d280c903ebb4d05614081767840778
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98830857"
---
# <a name="assertallzerowithintolerance-operation"></a><span data-ttu-id="ed878-102">Assertallzerowithintoleranz-Vorgang</span><span class="sxs-lookup"><span data-stu-id="ed878-102">AssertAllZeroWithinTolerance operation</span></span>

<span data-ttu-id="ed878-103">Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="ed878-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="ed878-104">Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="ed878-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="ed878-105">Bestätigen Sie, dass die angegebenen Qubits alle in $ \ket {0} $ State bis zu einer gegebenen Toleranz aufweisen.</span><span class="sxs-lookup"><span data-stu-id="ed878-105">Assert that given qubits are all in $\ket{0}$ state up to a given tolerance.</span></span>

```qsharp
operation AssertAllZeroWithinTolerance (qubits : Qubit[], tolerance : Double) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="ed878-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ed878-106">Input</span></span>

### <a name="qubits--qubit"></a><span data-ttu-id="ed878-107">Qubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="ed878-107">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="ed878-108">Qubits, die in $ \ket {0} $ State übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="ed878-108">Qubits that are asserted to be in $\ket{0}$ state.</span></span>


### <a name="tolerance--double"></a><span data-ttu-id="ed878-109">Toleranz: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="ed878-109">tolerance : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="ed878-110">Die Genauigkeit, mit der sich der Status in "$ \ket $ State" befinden sollte. {0}</span><span class="sxs-lookup"><span data-stu-id="ed878-110">Accuracy with which the state should be in $\ket{0}$ state</span></span>



## <a name="output--unit"></a><span data-ttu-id="ed878-111">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="ed878-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="ed878-112">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ed878-112">See Also</span></span>

- [<span data-ttu-id="ed878-113">Microsoft. Quantum. Diagnostics. assertqubitwithintoleranz</span><span class="sxs-lookup"><span data-stu-id="ed878-113">Microsoft.Quantum.Diagnostics.AssertQubitWithinTolerance</span></span>](xref:Microsoft.Quantum.Diagnostics.AssertQubitWithinTolerance)