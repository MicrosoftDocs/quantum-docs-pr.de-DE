---
uid: Microsoft.Quantum.Canon.ApplyControlledOnBitString
title: Applycontrolledonbitstring-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyControlledOnBitString
qsharp.summary: Applies a unitary operation on the target register, controlled on a a state specified by a given bit mask.
ms.openlocfilehash: 7a054511bacff574e6f7e889ace048c78886cf91
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705434"
---
# <a name="applycontrolledonbitstring-operation"></a><span data-ttu-id="86365-102">Applycontrolledonbitstring-Vorgang</span><span class="sxs-lookup"><span data-stu-id="86365-102">ApplyControlledOnBitString operation</span></span>

<span data-ttu-id="86365-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="86365-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="86365-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="86365-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="86365-105">Wendet einen einheitlichen Vorgang für das Ziel Register an, der in einem durch eine bestimmte Bitmaske angegebenen Zustand gesteuert wird.</span><span class="sxs-lookup"><span data-stu-id="86365-105">Applies a unitary operation on the target register, controlled on a a state specified by a given bit mask.</span></span>

```qsharp
operation ApplyControlledOnBitString<'T> (bits : Bool[], oracle : ('T => Unit is Adj + Ctl), controlRegister : Qubit[], targetRegister : 'T) : Unit
```


## <a name="input"></a><span data-ttu-id="86365-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="86365-106">Input</span></span>

### <a name="bits--bool"></a><span data-ttu-id="86365-107">Bits: [bool](xref:microsoft.quantum.lang-ref.bool)[]</span><span class="sxs-lookup"><span data-stu-id="86365-107">bits : [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span></span>

<span data-ttu-id="86365-108">Die Bitzeichenfolge, für die der angegebene einheitliche Vorgang gesteuert werden soll.</span><span class="sxs-lookup"><span data-stu-id="86365-108">The bit string to control the given unitary operation on.</span></span>


### <a name="oracle--t--unit-adj--ctl"></a><span data-ttu-id="86365-109">Oracle: 't => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="86365-109">oracle : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="86365-110">Der auf das Ziel Register anzuwendende einheitliche Vorgang.</span><span class="sxs-lookup"><span data-stu-id="86365-110">The unitary operation to be applied on the target register.</span></span>


### <a name="controlregister--qubit"></a><span data-ttu-id="86365-111">controlregister: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="86365-111">controlRegister : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="86365-112">Ein Quantum-Register, das die Anwendung von steuert `oracle` .</span><span class="sxs-lookup"><span data-stu-id="86365-112">A quantum register that controls application of `oracle`.</span></span>


### <a name="targetregister--t"></a><span data-ttu-id="86365-113">targetregiester: 't</span><span class="sxs-lookup"><span data-stu-id="86365-113">targetRegister : 'T</span></span>

<span data-ttu-id="86365-114">Das Ziel Register, das an als Eingabe an die übermittelt werden soll `oracle` .</span><span class="sxs-lookup"><span data-stu-id="86365-114">The target register to be passed to `oracle` as an input.</span></span>



## <a name="output--unit"></a><span data-ttu-id="86365-115">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="86365-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="86365-116">Typparameter</span><span class="sxs-lookup"><span data-stu-id="86365-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="86365-117">GIF</span><span class="sxs-lookup"><span data-stu-id="86365-117">'T</span></span>



## <a name="remarks"></a><span data-ttu-id="86365-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="86365-118">Remarks</span></span>

<span data-ttu-id="86365-119">Das von angegebene Muster `bits` ist möglicherweise kürzer als `controlRegister` . in diesem Fall werden zusätzliche Steuerungs-Qubits ignoriert (d. h., Sie werden nicht für "$ \ket {0} $" und "$ \ket $" gesteuert {1} ).</span><span class="sxs-lookup"><span data-stu-id="86365-119">The pattern given by `bits` may be shorter than `controlRegister`, in which case additional control qubits are ignored (that is, neither controlled on $\ket{0}$ nor $\ket{1}$).</span></span>
<span data-ttu-id="86365-120">Wenn `bits` länger als ist `controlRegister` , wird ein Fehler ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="86365-120">If `bits` is longer than `controlRegister`, an error is raised.</span></span>

<span data-ttu-id="86365-121">Beispielsweise `bits = [0,1,0,0,1]` bedeutet, dass `oracle` nur dann angewendet wird, wenn `controlRegister` sich im Zustand $ \ket {0} \ket {1} \ket \ket {0} {0} \ket {1} $ befindet.</span><span class="sxs-lookup"><span data-stu-id="86365-121">For example, `bits = [0,1,0,0,1]` means that `oracle` is applied if and only if `controlRegister` is in the state $\ket{0}\ket{1}\ket{0}\ket{0}\ket{1}$.</span></span>