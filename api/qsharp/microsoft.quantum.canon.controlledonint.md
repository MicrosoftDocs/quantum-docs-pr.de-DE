---
uid: Microsoft.Quantum.Canon.ControlledOnInt
title: Controlledonint-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ControlledOnInt
qsharp.summary: Returns a unitary operator that applies an oracle on the target register if the control register state corresponds to a specified positive integer.
ms.openlocfilehash: 3cc5c00d9c7295106901149e06571ef1963d1323
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96207257"
---
# <a name="controlledonint-function"></a><span data-ttu-id="771e4-102">Controlledonint-Funktion</span><span class="sxs-lookup"><span data-stu-id="771e4-102">ControlledOnInt function</span></span>

<span data-ttu-id="771e4-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="771e4-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="771e4-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="771e4-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="771e4-105">Gibt einen einheitlichen Operator zurück, der ein Oracle auf das Ziel Register anwendet, wenn der Steuerelement Registrierungs Zustand einer angegebenen positiven ganzen Zahl entspricht.</span><span class="sxs-lookup"><span data-stu-id="771e4-105">Returns a unitary operator that applies an oracle on the target register if the control register state corresponds to a specified positive integer.</span></span>

```qsharp
function ControlledOnInt<'T> (numberState : Int, oracle : ('T => Unit is Adj + Ctl)) : ((Qubit[], 'T) => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="771e4-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="771e4-106">Input</span></span>

### <a name="numberstate--int"></a><span data-ttu-id="771e4-107">numstate: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="771e4-107">numberState : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="771e4-108">Positive Ganzzahl.</span><span class="sxs-lookup"><span data-stu-id="771e4-108">Positive integer.</span></span>


### <a name="oracle--t--unit--is-adj--ctl"></a><span data-ttu-id="771e4-109">Oracle: 't => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="771e4-109">oracle : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="771e4-110">Einheitlicher Operator.</span><span class="sxs-lookup"><span data-stu-id="771e4-110">Unitary operator.</span></span>



## <a name="output--qubitt--unit--is-adj--ctl"></a><span data-ttu-id="771e4-111">Ausgabe: ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[], 't) => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="771e4-111">Output : ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[],'T) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="771e4-112">Ein einheitlicher Operator, `oracle` der auf das Ziel Register angewendet wird, wenn der Registrierungs Zustand des Steuer Elements dem Zahlen Zustand entspricht `numberState` .</span><span class="sxs-lookup"><span data-stu-id="771e4-112">A unitary operator that applies `oracle` on the target register if the control register state corresponds to the number state `numberState`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="771e4-113">Typparameter</span><span class="sxs-lookup"><span data-stu-id="771e4-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="771e4-114">GIF</span><span class="sxs-lookup"><span data-stu-id="771e4-114">'T</span></span>



## <a name="remarks"></a><span data-ttu-id="771e4-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="771e4-115">Remarks</span></span>

<span data-ttu-id="771e4-116">Der Wert von `numberState` wird mithilfe einer Little-enumdian-Codierung interpretiert.</span><span class="sxs-lookup"><span data-stu-id="771e4-116">The value of `numberState` is interpreted using a little-endian encoding.</span></span>