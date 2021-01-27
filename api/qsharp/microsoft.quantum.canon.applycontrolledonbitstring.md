---
uid: Microsoft.Quantum.Canon.ApplyControlledOnBitString
title: Applycontrolledonbitstring-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyControlledOnBitString
qsharp.summary: Applies a unitary operation on the target register, controlled on a a state specified by a given bit mask.
ms.openlocfilehash: 82adc74e23e1d50cb6436176a973fdd1a0eeb3bd
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841947"
---
# <a name="applycontrolledonbitstring-operation"></a><span data-ttu-id="7fe95-102">Applycontrolledonbitstring-Vorgang</span><span class="sxs-lookup"><span data-stu-id="7fe95-102">ApplyControlledOnBitString operation</span></span>

<span data-ttu-id="7fe95-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="7fe95-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="7fe95-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="7fe95-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="7fe95-105">Wendet einen einheitlichen Vorgang für das Ziel Register an, der in einem durch eine bestimmte Bitmaske angegebenen Zustand gesteuert wird.</span><span class="sxs-lookup"><span data-stu-id="7fe95-105">Applies a unitary operation on the target register, controlled on a a state specified by a given bit mask.</span></span>

```qsharp
operation ApplyControlledOnBitString<'T> (bits : Bool[], oracle : ('T => Unit is Adj + Ctl), controlRegister : Qubit[], targetRegister : 'T) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="7fe95-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="7fe95-106">Input</span></span>

### <a name="bits--bool"></a><span data-ttu-id="7fe95-107">Bits: [bool](xref:microsoft.quantum.lang-ref.bool)[]</span><span class="sxs-lookup"><span data-stu-id="7fe95-107">bits : [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span></span>

<span data-ttu-id="7fe95-108">Die Bitzeichenfolge, für die der angegebene einheitliche Vorgang gesteuert werden soll.</span><span class="sxs-lookup"><span data-stu-id="7fe95-108">The bit string to control the given unitary operation on.</span></span>


### <a name="oracle--t--unit--is-adj--ctl"></a><span data-ttu-id="7fe95-109">Oracle: 't => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="7fe95-109">oracle : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="7fe95-110">Der auf das Ziel Register anzuwendende einheitliche Vorgang.</span><span class="sxs-lookup"><span data-stu-id="7fe95-110">The unitary operation to be applied on the target register.</span></span>


### <a name="controlregister--qubit"></a><span data-ttu-id="7fe95-111">controlregister: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="7fe95-111">controlRegister : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="7fe95-112">Ein Quantum-Register, das die Anwendung von steuert `oracle` .</span><span class="sxs-lookup"><span data-stu-id="7fe95-112">A quantum register that controls application of `oracle`.</span></span>


### <a name="targetregister--t"></a><span data-ttu-id="7fe95-113">targetregiester: 't</span><span class="sxs-lookup"><span data-stu-id="7fe95-113">targetRegister : 'T</span></span>

<span data-ttu-id="7fe95-114">Das Ziel Register, das an als Eingabe an die übermittelt werden soll `oracle` .</span><span class="sxs-lookup"><span data-stu-id="7fe95-114">The target register to be passed to `oracle` as an input.</span></span>



## <a name="output--unit"></a><span data-ttu-id="7fe95-115">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="7fe95-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="7fe95-116">Typparameter</span><span class="sxs-lookup"><span data-stu-id="7fe95-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="7fe95-117">GIF</span><span class="sxs-lookup"><span data-stu-id="7fe95-117">'T</span></span>



## <a name="remarks"></a><span data-ttu-id="7fe95-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7fe95-118">Remarks</span></span>

<span data-ttu-id="7fe95-119">Das von angegebene Muster `bits` ist möglicherweise kürzer als `controlRegister` . in diesem Fall werden zusätzliche Steuerungs-Qubits ignoriert (d. h., Sie werden nicht für "$ \ket {0} $" und "$ \ket $" gesteuert {1} ).</span><span class="sxs-lookup"><span data-stu-id="7fe95-119">The pattern given by `bits` may be shorter than `controlRegister`, in which case additional control qubits are ignored (that is, neither controlled on $\ket{0}$ nor $\ket{1}$).</span></span>
<span data-ttu-id="7fe95-120">Wenn `bits` länger als ist `controlRegister` , wird ein Fehler ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="7fe95-120">If `bits` is longer than `controlRegister`, an error is raised.</span></span>

<span data-ttu-id="7fe95-121">Beispielsweise `bits = [0,1,0,0,1]` bedeutet, dass `oracle` nur dann angewendet wird, wenn `controlRegister` sich im Zustand $ \ket {0} \ket {1} \ket \ket {0} {0} \ket {1} $ befindet.</span><span class="sxs-lookup"><span data-stu-id="7fe95-121">For example, `bits = [0,1,0,0,1]` means that `oracle` is applied if and only if `controlRegister` is in the state $\ket{0}\ket{1}\ket{0}\ket{0}\ket{1}$.</span></span>