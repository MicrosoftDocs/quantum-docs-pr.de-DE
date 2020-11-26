---
uid: Microsoft.Quantum.Canon.ControlledOnBitString
title: Controlledonbitstring-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ControlledOnBitString
qsharp.summary: Returns a unitary operation that applies an oracle on the target register if the control register state corresponds to a specified bit mask.
ms.openlocfilehash: 9435406506fc99fe211f5dce628b21c18ee4f9fe
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96216658"
---
# <a name="controlledonbitstring-function"></a><span data-ttu-id="8fc73-102">Controlledonbitstring-Funktion</span><span class="sxs-lookup"><span data-stu-id="8fc73-102">ControlledOnBitString function</span></span>

<span data-ttu-id="8fc73-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="8fc73-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="8fc73-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="8fc73-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="8fc73-105">Gibt einen einheitlichen Vorgang zurück, der ein Oracle auf das Ziel Register anwendet, wenn der Steuerelement Registrierungs Zustand einer angegebenen Bitmaske entspricht.</span><span class="sxs-lookup"><span data-stu-id="8fc73-105">Returns a unitary operation that applies an oracle on the target register if the control register state corresponds to a specified bit mask.</span></span>

```qsharp
function ControlledOnBitString<'T> (bits : Bool[], oracle : ('T => Unit is Adj + Ctl)) : ((Qubit[], 'T) => Unit is Adj + Ctl)
```


## <a name="description"></a><span data-ttu-id="8fc73-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8fc73-106">Description</span></span>

<span data-ttu-id="8fc73-107">Die Ausgabe dieser Funktion ist ein Vorgang, der durch eine einheitliche Transformation $U $ dargestellt werden kann, sodass \begin{align} U \ket{b_0 B_1 \cdots b_ {n-1}} \ket{\psi} = \ket{b_0 B_1 \cdots b_ {n-1}} \otimes \begin{Cases} V \ket{\psi} & \textrm{if} (b_0 B_1 \cdots b_ {n-1}) = \texttt{Bits} \\ \\ \ket{\psi} & \textrm{otherwits} \end{Cases}, \end{align}, wobei $V $ eine einheitliche Transformation ist, die die Aktion des `oracle` Vorgangs darstellt.</span><span class="sxs-lookup"><span data-stu-id="8fc73-107">The output of this function is an operation that can be represented by a unitary transformation $U$ such that \begin{align} U \ket{b_0 b_1 \cdots b_{n - 1}} \ket{\psi} = \ket{b_0 b_1 \cdots b_{n-1}} \otimes \begin{cases} V \ket{\psi} & \textrm{if} (b_0 b_1 \cdots b_{n - 1}) = \texttt{bits} \\\\ \ket{\psi} & \textrm{otherwise} \end{cases}, \end{align} where $V$ is a unitary transformation that represents the action of the `oracle` operation.</span></span>

## <a name="input"></a><span data-ttu-id="8fc73-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8fc73-108">Input</span></span>

### <a name="bits--bool"></a><span data-ttu-id="8fc73-109">Bits: [bool](xref:microsoft.quantum.lang-ref.bool)[]</span><span class="sxs-lookup"><span data-stu-id="8fc73-109">bits : [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span></span>

<span data-ttu-id="8fc73-110">Die Bitzeichenfolge, für die der angegebene einheitliche Vorgang gesteuert werden soll.</span><span class="sxs-lookup"><span data-stu-id="8fc73-110">The bit string to control the given unitary operation on.</span></span>


### <a name="oracle--t--unit--is-adj--ctl"></a><span data-ttu-id="8fc73-111">Oracle: 't => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="8fc73-111">oracle : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="8fc73-112">Der auf das Ziel Register anzuwendende einheitliche Vorgang.</span><span class="sxs-lookup"><span data-stu-id="8fc73-112">The unitary operation to be applied on the target register.</span></span>



## <a name="output--qubitt--unit--is-adj--ctl"></a><span data-ttu-id="8fc73-113">Ausgabe: ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[], 't) => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="8fc73-113">Output : ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[],'T) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="8fc73-114">Ein einheitlicher Vorgang, `oracle` der für das Ziel Register gilt, wenn der Steuerelement Registrierungs Zustand der Bitmaske entspricht `bits` .</span><span class="sxs-lookup"><span data-stu-id="8fc73-114">A unitary operation that applies `oracle` on the target register if the control register state corresponds to the bit mask `bits`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="8fc73-115">Typparameter</span><span class="sxs-lookup"><span data-stu-id="8fc73-115">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="8fc73-116">GIF</span><span class="sxs-lookup"><span data-stu-id="8fc73-116">'T</span></span>



## <a name="remarks"></a><span data-ttu-id="8fc73-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8fc73-117">Remarks</span></span>

<span data-ttu-id="8fc73-118">Das von angegebene Muster `bits` ist möglicherweise kürzer als `controlRegister` . in diesem Fall werden zusätzliche Steuerungs-Qubits ignoriert (d. h., Sie werden nicht für "$ \ket {0} $" und "$ \ket $" gesteuert {1} ).</span><span class="sxs-lookup"><span data-stu-id="8fc73-118">The pattern given by `bits` may be shorter than `controlRegister`, in which case additional control qubits are ignored (that is, neither controlled on $\ket{0}$ nor $\ket{1}$).</span></span>
<span data-ttu-id="8fc73-119">Wenn `bits` länger als ist `controlRegister` , wird ein Fehler ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="8fc73-119">If `bits` is longer than `controlRegister`, an error is raised.</span></span>

<span data-ttu-id="8fc73-120">Bei einem booleschen Array `bits` und einem einheitlichen Vorgang `oracle` ist die Ausgabe dieser Funktion ein Vorgang, der die folgenden Schritte ausführt:</span><span class="sxs-lookup"><span data-stu-id="8fc73-120">Given a Boolean array `bits` and a unitary operation `oracle`, the output of this function is an operation that performs the following steps:</span></span>

* <span data-ttu-id="8fc73-121">wenden `X` Sie einen Vorgang auf jedes Qubit des Steuerelement Registrierungs Elements an, das dem- `false` Element von entspricht `bits` .</span><span class="sxs-lookup"><span data-stu-id="8fc73-121">apply an `X` operation to each qubit of the control register that corresponds to `false` element of the `bits`;</span></span>
* <span data-ttu-id="8fc73-122">`Controlled oracle`auf das Steuerelement und die Ziel Register anwenden;</span><span class="sxs-lookup"><span data-stu-id="8fc73-122">apply `Controlled oracle` to the control and target registers;</span></span>
* <span data-ttu-id="8fc73-123">wenden `X` Sie einen Vorgang auf jedes Qubit des Steuerelement Registrierungs Elements an, das dem- `false` Element des-Elements entspricht, `bits` um das Steuerelement in den ursprünglichen Zustand zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="8fc73-123">apply an `X` operation to each qubit of the control register that corresponds to `false` element of the `bits` again to return the control register to the original state.</span></span>

<span data-ttu-id="8fc73-124">Die Ausgabe des `Controlled` funktors ist ein Sonderfall von `ControlledOnBitString` , wobei `bits` gleich ist `[true, ..., true]` .</span><span class="sxs-lookup"><span data-stu-id="8fc73-124">The output of the `Controlled` functor is a special case of `ControlledOnBitString` where `bits` is equal to `[true, ..., true]`.</span></span>