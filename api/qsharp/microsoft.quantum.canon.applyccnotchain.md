---
uid: Microsoft.Quantum.Canon.ApplyCCNOTChain
title: Applyccnotchain-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyCCNOTChain
qsharp.summary: Implements a cascade of CCNOT gates controlled on corresponding bits of two qubit registers, acting on the next qubit of one of the registers. Starting from the qubits at position 0 in both registers as controls, CCNOT is applied to the qubit at position 1 of the target register, then controlled by the qubits at position 1 acting on the qubit at position 2 in the target register, etc., ending with an action on the target qubit in position `Length(nQubits)-1`.
ms.openlocfilehash: 53fdd59b06d542494647acb665f248fc18de93d9
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845137"
---
# <a name="applyccnotchain-operation"></a><span data-ttu-id="e240e-102">Applyccnotchain-Vorgang</span><span class="sxs-lookup"><span data-stu-id="e240e-102">ApplyCCNOTChain operation</span></span>

<span data-ttu-id="e240e-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="e240e-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="e240e-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="e240e-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="e240e-105">Implementiert eine Cascade von ccnot Gates, die für die entsprechenden Bits zweier Qubit-Register gesteuert werden, und verhält sich für das nächste Qubit eines der Register.</span><span class="sxs-lookup"><span data-stu-id="e240e-105">Implements a cascade of CCNOT gates controlled on corresponding bits of two qubit registers, acting on the next qubit of one of the registers.</span></span>
<span data-ttu-id="e240e-106">Beginnend mit den Qubits an Position 0 in beiden Registern als Steuerelemente, wird ccnot auf das Qubit an Position 1 des Ziel Registers angewendet und dann von den Qubits an Position 1 gesteuert, die auf dem Qubit an Position 2 im Zielregister agiert, usw., und endet mit einer Aktion auf dem Ziel-Qubit an der Position `Length(nQubits)-1` .</span><span class="sxs-lookup"><span data-stu-id="e240e-106">Starting from the qubits at position 0 in both registers as controls, CCNOT is applied to the qubit at position 1 of the target register, then controlled by the qubits at position 1 acting on the qubit at position 2 in the target register, etc., ending with an action on the target qubit in position `Length(nQubits)-1`.</span></span>

```qsharp
operation ApplyCCNOTChain (register : Qubit[], targets : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="e240e-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e240e-107">Input</span></span>

### <a name="register--qubit"></a><span data-ttu-id="e240e-108">Register: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="e240e-108">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="e240e-109">Das Qubit-Register wird nur für Steuerelemente verwendet.</span><span class="sxs-lookup"><span data-stu-id="e240e-109">Qubit register, only used for controls.</span></span>


### <a name="targets--qubit"></a><span data-ttu-id="e240e-110">Ziele: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="e240e-110">targets : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="e240e-111">Ein Qubit-Register, das für Steuerelemente und als Ziel verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e240e-111">Qubit register, used for controls and as target.</span></span>



## <a name="output--unit"></a><span data-ttu-id="e240e-112">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="e240e-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="e240e-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e240e-113">Remarks</span></span>

<span data-ttu-id="e240e-114">Für das Ziel-Qubit-Register muss ein Qubit mehr als das andere Register vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="e240e-114">The target qubit register must have one qubit more than the other register.</span></span>