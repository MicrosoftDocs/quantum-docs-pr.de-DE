---
uid: Microsoft.Quantum.Canon.ApplyMultiControlledC
title: Applymulticontrolledc-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyMultiControlledC
qsharp.summary: Applies a multiply controlled version of a singly controlled operation. The modifier `C` indicates that the single-qubit operation is controllable.
ms.openlocfilehash: 2d5703eed3a3b6e611ae7c993febf018fcb148b3
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96218409"
---
# <a name="applymulticontrolledc-operation"></a><span data-ttu-id="7cd2c-102">Applymulticontrolledc-Vorgang</span><span class="sxs-lookup"><span data-stu-id="7cd2c-102">ApplyMultiControlledC operation</span></span>

<span data-ttu-id="7cd2c-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="7cd2c-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="7cd2c-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="7cd2c-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="7cd2c-105">Wendet eine mehrfach gesteuerte Version eines einzeln kontrollierten Vorgangs an.</span><span class="sxs-lookup"><span data-stu-id="7cd2c-105">Applies a multiply controlled version of a singly controlled operation.</span></span>
<span data-ttu-id="7cd2c-106">Der-Modifizierer `C` gibt an, dass der Single-Qubit-Vorgang steuerbar ist.</span><span class="sxs-lookup"><span data-stu-id="7cd2c-106">The modifier `C` indicates that the single-qubit operation is controllable.</span></span>

```qsharp
operation ApplyMultiControlledC (singlyControlledOp : (Qubit[] => Unit), ccnot : Microsoft.Quantum.Canon.CCNOTop, controls : Qubit[], targets : Qubit[]) : Unit is Ctl
```


## <a name="input"></a><span data-ttu-id="7cd2c-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="7cd2c-107">Input</span></span>

### <a name="singlycontrolledop--qubit--unit"></a><span data-ttu-id="7cd2c-108">singlycontrolledop: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="7cd2c-108">singlyControlledOp : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="7cd2c-109">Ein Vorgang, der auf einem einzelnen Qubit gesteuert wird.</span><span class="sxs-lookup"><span data-stu-id="7cd2c-109">An operation controlled on a single qubit.</span></span>
<span data-ttu-id="7cd2c-110">Bei dem ersten Qubit im-Argument des Vorgangs wird angenommen, dass es sich um ein-Steuerelement handelt, und der Rest wird als Ziel-Qubits angenommen.</span><span class="sxs-lookup"><span data-stu-id="7cd2c-110">The first qubit in the argument of the operation is assumed to be a control and the rest are assumed to be target qubits.</span></span>
<span data-ttu-id="7cd2c-111">`ApplyMultiControlled` Ruft immer `singlyControlledOp` mit einem Argument der Länge von mindestens 1 auf.</span><span class="sxs-lookup"><span data-stu-id="7cd2c-111">`ApplyMultiControlled` always calls `singlyControlledOp` with an argument of length at least 1.</span></span>


### <a name="ccnot--ccnotop"></a><span data-ttu-id="7cd2c-112">ccnot: [ccnotop](xref:Microsoft.Quantum.Canon.CCNOTop)</span><span class="sxs-lookup"><span data-stu-id="7cd2c-112">ccnot : [CCNOTop](xref:Microsoft.Quantum.Canon.CCNOTop)</span></span>

<span data-ttu-id="7cd2c-113">Das für die Konstruktion zu verwendende gesteuerte-not-Gate.</span><span class="sxs-lookup"><span data-stu-id="7cd2c-113">The controlled-controlled-NOT gate to use for the construction.</span></span>


### <a name="controls--qubit"></a><span data-ttu-id="7cd2c-114">Steuerelemente: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="7cd2c-114">controls : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="7cd2c-115">Die Qubits, die `singlyControlledOp` gesteuert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="7cd2c-115">The qubits that `singlyControlledOp` is to be controlled on.</span></span>
<span data-ttu-id="7cd2c-116">Die Länge von `controls` muss mindestens 1 betragen.</span><span class="sxs-lookup"><span data-stu-id="7cd2c-116">The length of `controls` must be at least 1.</span></span>


### <a name="targets--qubit"></a><span data-ttu-id="7cd2c-117">Ziele: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="7cd2c-117">targets : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="7cd2c-118">Die Ziel-Qubits, die auf angewendet werden `singlyControlledOp` .</span><span class="sxs-lookup"><span data-stu-id="7cd2c-118">The target qubits that `singlyControlledOp` acts upon.</span></span>



## <a name="output--unit"></a><span data-ttu-id="7cd2c-119">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="7cd2c-119">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="7cd2c-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7cd2c-120">Remarks</span></span>

<span data-ttu-id="7cd2c-121">Bei diesem Vorgang werden nur saubere Ancilla-Qubits verwendet.</span><span class="sxs-lookup"><span data-stu-id="7cd2c-121">This operation uses only clean ancilla qubits.</span></span>

<span data-ttu-id="7cd2c-122">Eine Erläuterung und ein Leitungs Diagramm finden Sie in Abbildung 4,10, Abschnitt 4,3 in Nielsen & Chuang.</span><span class="sxs-lookup"><span data-stu-id="7cd2c-122">For the explanation and circuit diagram see Figure 4.10, Section 4.3 in Nielsen & Chuang</span></span>

## <a name="references"></a><span data-ttu-id="7cd2c-123">Referenzen</span><span class="sxs-lookup"><span data-stu-id="7cd2c-123">References</span></span>

- [<span data-ttu-id="7cd2c-124">*Michael A. Nielsen, ISAL. Chuang*, Quantum-Berechnung und Quantum-Informationen</span><span class="sxs-lookup"><span data-stu-id="7cd2c-124"> *Michael A. Nielsen , Isaac L. Chuang*, Quantum Computation and Quantum Information </span></span>](http://doi.org/10.1017/CBO9780511976667)

## <a name="see-also"></a><span data-ttu-id="7cd2c-125">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="7cd2c-125">See Also</span></span>

- [<span data-ttu-id="7cd2c-126">Microsoft. Quantum. Canon. applymulticontrolledca</span><span class="sxs-lookup"><span data-stu-id="7cd2c-126">Microsoft.Quantum.Canon.ApplyMultiControlledCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyMultiControlledCA)