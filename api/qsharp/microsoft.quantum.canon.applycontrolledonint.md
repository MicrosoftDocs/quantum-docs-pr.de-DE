---
uid: Microsoft.Quantum.Canon.ApplyControlledOnInt
title: Applycontrolledonint-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyControlledOnInt
qsharp.summary: Applies a unitary operation on the target register if the control register state corresponds to a specified positive integer.
ms.openlocfilehash: 499a25104742b2d03886065baad4d535ea92e83b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845099"
---
# <a name="applycontrolledonint-operation"></a><span data-ttu-id="82ea3-102">Applycontrolledonint-Vorgang</span><span class="sxs-lookup"><span data-stu-id="82ea3-102">ApplyControlledOnInt operation</span></span>

<span data-ttu-id="82ea3-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="82ea3-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="82ea3-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="82ea3-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="82ea3-105">Wendet einen einheitlichen Vorgang auf das Ziel Register an, wenn der Steuerelement Registrierungs Zustand einer angegebenen positiven ganzen Zahl entspricht.</span><span class="sxs-lookup"><span data-stu-id="82ea3-105">Applies a unitary operation on the target register if the control register state corresponds to a specified positive integer.</span></span>

```qsharp
operation ApplyControlledOnInt<'T> (numberState : Int, oracle : ('T => Unit is Adj + Ctl), controlRegister : Qubit[], targetRegister : 'T) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="82ea3-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="82ea3-106">Input</span></span>

### <a name="numberstate--int"></a><span data-ttu-id="82ea3-107">numstate: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="82ea3-107">numberState : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="82ea3-108">Eine nicht negative ganze Zahl, für die der Vorgang `oracle` gesteuert werden soll.</span><span class="sxs-lookup"><span data-stu-id="82ea3-108">A nonnegative integer on which the operation `oracle` should be controlled.</span></span>


### <a name="oracle--t--unit--is-adj--ctl"></a><span data-ttu-id="82ea3-109">Oracle: 't => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="82ea3-109">oracle : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="82ea3-110">Ein einheitlicher Vorgang, der gesteuert werden soll.</span><span class="sxs-lookup"><span data-stu-id="82ea3-110">A unitary operation to be controlled.</span></span>


### <a name="controlregister--qubit"></a><span data-ttu-id="82ea3-111">controlregister: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="82ea3-111">controlRegister : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="82ea3-112">Ein Quantum-Register, das die Anwendung von steuert `oracle` .</span><span class="sxs-lookup"><span data-stu-id="82ea3-112">A quantum register that controls application of `oracle`.</span></span>


### <a name="targetregister--t"></a><span data-ttu-id="82ea3-113">targetregiester: 't</span><span class="sxs-lookup"><span data-stu-id="82ea3-113">targetRegister : 'T</span></span>

<span data-ttu-id="82ea3-114">Ein Register, das angewendet werden soll `oracle` .</span><span class="sxs-lookup"><span data-stu-id="82ea3-114">A register on which to apply `oracle`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="82ea3-115">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="82ea3-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="82ea3-116">Typparameter</span><span class="sxs-lookup"><span data-stu-id="82ea3-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="82ea3-117">GIF</span><span class="sxs-lookup"><span data-stu-id="82ea3-117">'T</span></span>



## <a name="remarks"></a><span data-ttu-id="82ea3-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="82ea3-118">Remarks</span></span>

<span data-ttu-id="82ea3-119">Der Wert von `numberState` wird mithilfe einer Little-enumdian-Codierung interpretiert.</span><span class="sxs-lookup"><span data-stu-id="82ea3-119">The value of `numberState` is interpreted using a little-endian encoding.</span></span>

<span data-ttu-id="82ea3-120">`numberState` muss höchstens $2 ^ \texttt{length (controlregister)}-$1.</span><span class="sxs-lookup"><span data-stu-id="82ea3-120">`numberState` must be at most $2^\texttt{Length(controlRegister)} - 1$.</span></span>
<span data-ttu-id="82ea3-121">Beispielsweise `numberState = 537` bedeutet, dass `oracle` nur dann angewendet wird, wenn `controlRegister` sich im Zustand $ \ket {537} $ befindet.</span><span class="sxs-lookup"><span data-stu-id="82ea3-121">For example, `numberState = 537` means that `oracle` is applied if and only if `controlRegister` is in the state $\ket{537}$.</span></span>