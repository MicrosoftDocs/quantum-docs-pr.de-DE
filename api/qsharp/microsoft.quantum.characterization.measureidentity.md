---
uid: Microsoft.Quantum.Characterization.MeasureIdentity
title: Measureidentity-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: MeasureIdentity
qsharp.summary: Measures the identity operator on a register of qubits.
ms.openlocfilehash: 4a169355d0669c67f0eb14c80e8554b2f24b035a
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96216114"
---
# <a name="measureidentity-operation"></a><span data-ttu-id="7ae3b-102">Measureidentity-Vorgang</span><span class="sxs-lookup"><span data-stu-id="7ae3b-102">MeasureIdentity operation</span></span>

<span data-ttu-id="7ae3b-103">Namespace: [Microsoft. Quantum. Charakterisierung](xref:Microsoft.Quantum.Characterization)</span><span class="sxs-lookup"><span data-stu-id="7ae3b-103">Namespace: [Microsoft.Quantum.Characterization](xref:Microsoft.Quantum.Characterization)</span></span>

<span data-ttu-id="7ae3b-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="7ae3b-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="7ae3b-105">Misst den Identitäts Operator für ein Register von Qubits.</span><span class="sxs-lookup"><span data-stu-id="7ae3b-105">Measures the identity operator on a register of qubits.</span></span>

```qsharp
operation MeasureIdentity (register : Qubit[]) : Result
```


## <a name="input"></a><span data-ttu-id="7ae3b-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="7ae3b-106">Input</span></span>

### <a name="register--qubit"></a><span data-ttu-id="7ae3b-107">Register: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="7ae3b-107">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="7ae3b-108">Das zu messende Register.</span><span class="sxs-lookup"><span data-stu-id="7ae3b-108">The register to be measured.</span></span>



## <a name="output--__invalidresult__"></a><span data-ttu-id="7ae3b-109">Ausgabe: __ungültig <Result>__</span><span class="sxs-lookup"><span data-stu-id="7ae3b-109">Output : __invalid<Result>__</span></span>

<span data-ttu-id="7ae3b-110">Der Ergebniswert `Zero` .</span><span class="sxs-lookup"><span data-stu-id="7ae3b-110">The result value `Zero`.</span></span>

## <a name="remarks"></a><span data-ttu-id="7ae3b-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7ae3b-111">Remarks</span></span>

<span data-ttu-id="7ae3b-112">Da $ \boldone $ nur den eigen Wert $1 $ und keinen negativen eigen Wert aufweist, gibt dieser Vorgang immer zurück `Zero` , was dem Eigen Wert $ + 1 = (-1) ^ 0 $ entspricht, und führt nicht zu einem zuklappen des Zustands von `register` .</span><span class="sxs-lookup"><span data-stu-id="7ae3b-112">Since $\boldone$ has only the eigenvalue $1$, and does not have a negative eigenvalue, this operation always returns `Zero`, corresponding to the eigenvalue $+1 = (-1)^0$, and does not cause a collapse of the state of `register`.</span></span>

<span data-ttu-id="7ae3b-113">Dieser Vorgang ist zwar nicht sinnvoll, aber im Kontext der Prozess Tomographie hilfreich, da er Informationen über die Beibehaltung der Ablauf Verfolgung eines Quantum-Prozesses bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="7ae3b-113">On its own, this operation is not useful, but is helpful in the context of process tomography, as it provides information about the trace preservation of a quantum process.</span></span>
<span data-ttu-id="7ae3b-114">Vor allem sollte ein Zielcomputer mit Verlust Messung diesen Vorgang durch eine tatsächliche Messung von $ \boldone $ ersetzen.</span><span class="sxs-lookup"><span data-stu-id="7ae3b-114">In particular, a target machine with lossy measurement should replace this operation by an actual measurement of $\boldone$.</span></span>