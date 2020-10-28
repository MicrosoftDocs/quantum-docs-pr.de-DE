---
uid: Microsoft.Quantum.Canon.ControlledOnInt
title: Controlledonint-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ControlledOnInt
qsharp.summary: Returns a unitary operator that applies an oracle on the target register if the control register state corresponds to a specified positive integer.
ms.openlocfilehash: 4c48f3257f91fc50040d02cae7c2f7bdf87ea7c5
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704311"
---
# <a name="controlledonint-function"></a><span data-ttu-id="9bea0-102">Controlledonint-Funktion</span><span class="sxs-lookup"><span data-stu-id="9bea0-102">ControlledOnInt function</span></span>

<span data-ttu-id="9bea0-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="9bea0-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="9bea0-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="9bea0-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="9bea0-105">Gibt einen einheitlichen Operator zurück, der ein Oracle auf das Ziel Register anwendet, wenn der Steuerelement Registrierungs Zustand einer angegebenen positiven ganzen Zahl entspricht.</span><span class="sxs-lookup"><span data-stu-id="9bea0-105">Returns a unitary operator that applies an oracle on the target register if the control register state corresponds to a specified positive integer.</span></span>

```qsharp
function ControlledOnInt<'T> (numberState : Int, oracle : ('T => Unit is Adj + Ctl)) : ((Qubit[], 'T) => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="9bea0-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="9bea0-106">Input</span></span>

### <a name="numberstate--int"></a><span data-ttu-id="9bea0-107">numstate: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="9bea0-107">numberState : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="9bea0-108">Positive Ganzzahl.</span><span class="sxs-lookup"><span data-stu-id="9bea0-108">Positive integer.</span></span>


### <a name="oracle--t--unit-adj--ctl"></a><span data-ttu-id="9bea0-109">Oracle: 't => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="9bea0-109">oracle : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="9bea0-110">Einheitlicher Operator.</span><span class="sxs-lookup"><span data-stu-id="9bea0-110">Unitary operator.</span></span>



## <a name="output--qubitt--unit-adj--ctl"></a><span data-ttu-id="9bea0-111">Ausgabe: ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[], 't) => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="9bea0-111">Output : ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[],'T) => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="9bea0-112">Ein einheitlicher Operator, `oracle` der auf das Ziel Register angewendet wird, wenn der Registrierungs Zustand des Steuer Elements dem Zahlen Zustand entspricht `numberState` .</span><span class="sxs-lookup"><span data-stu-id="9bea0-112">A unitary operator that applies `oracle` on the target register if the control register state corresponds to the number state `numberState`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="9bea0-113">Typparameter</span><span class="sxs-lookup"><span data-stu-id="9bea0-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="9bea0-114">GIF</span><span class="sxs-lookup"><span data-stu-id="9bea0-114">'T</span></span>



## <a name="remarks"></a><span data-ttu-id="9bea0-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9bea0-115">Remarks</span></span>

<span data-ttu-id="9bea0-116">Der Wert von `numberState` wird mithilfe einer Little-enumdian-Codierung interpretiert.</span><span class="sxs-lookup"><span data-stu-id="9bea0-116">The value of `numberState` is interpreted using a little-endian encoding.</span></span>