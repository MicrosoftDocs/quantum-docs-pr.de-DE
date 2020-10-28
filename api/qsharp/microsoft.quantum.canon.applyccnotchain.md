---
uid: Microsoft.Quantum.Canon.ApplyCCNOTChain
title: Applyccnotchain-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyCCNOTChain
qsharp.summary: Implements a cascade of CCNOT gates controlled on corresponding bits of two qubit registers, acting on the next qubit of one of the registers. Starting from the qubits at position 0 in both registers as controls, CCNOT is applied to the qubit at position 1 of the target register, then controlled by the qubits at position 1 acting on the qubit at position 2 in the target register, etc., ending with an action on the target qubit in position `Length(nQubits)-1`.
ms.openlocfilehash: e4f38e9bb54839076b817f6e61e96ca6a550576b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705455"
---
# <a name="applyccnotchain-operation"></a><span data-ttu-id="d5098-102">Applyccnotchain-Vorgang</span><span class="sxs-lookup"><span data-stu-id="d5098-102">ApplyCCNOTChain operation</span></span>

<span data-ttu-id="d5098-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="d5098-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="d5098-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="d5098-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="d5098-105">Implementiert eine Cascade von ccnot Gates, die für die entsprechenden Bits zweier Qubit-Register gesteuert werden, und verhält sich für das nächste Qubit eines der Register.</span><span class="sxs-lookup"><span data-stu-id="d5098-105">Implements a cascade of CCNOT gates controlled on corresponding bits of two qubit registers, acting on the next qubit of one of the registers.</span></span>
<span data-ttu-id="d5098-106">Beginnend mit den Qubits an Position 0 in beiden Registern als Steuerelemente, wird ccnot auf das Qubit an Position 1 des Ziel Registers angewendet und dann von den Qubits an Position 1 gesteuert, die auf dem Qubit an Position 2 im Zielregister agiert, usw., und endet mit einer Aktion auf dem Ziel-Qubit an der Position `Length(nQubits)-1` .</span><span class="sxs-lookup"><span data-stu-id="d5098-106">Starting from the qubits at position 0 in both registers as controls, CCNOT is applied to the qubit at position 1 of the target register, then controlled by the qubits at position 1 acting on the qubit at position 2 in the target register, etc., ending with an action on the target qubit in position `Length(nQubits)-1`.</span></span>

```qsharp
operation ApplyCCNOTChain (register : Qubit[], targets : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="d5098-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d5098-107">Input</span></span>

### <a name="register--qubit"></a><span data-ttu-id="d5098-108">Register: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="d5098-108">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="d5098-109">Das Qubit-Register wird nur für Steuerelemente verwendet.</span><span class="sxs-lookup"><span data-stu-id="d5098-109">Qubit register, only used for controls.</span></span>


### <a name="targets--qubit"></a><span data-ttu-id="d5098-110">Ziele: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="d5098-110">targets : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="d5098-111">Ein Qubit-Register, das für Steuerelemente und als Ziel verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d5098-111">Qubit register, used for controls and as target.</span></span>



## <a name="output--unit"></a><span data-ttu-id="d5098-112">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="d5098-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="d5098-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d5098-113">Remarks</span></span>

<span data-ttu-id="d5098-114">Für das Ziel-Qubit-Register muss ein Qubit mehr als das andere Register vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="d5098-114">The target qubit register must have one qubit more than the other register.</span></span>