---
uid: Microsoft.Quantum.Canon.ControlledOnInt
title: Controlledonint-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ControlledOnInt
qsharp.summary: Returns a unitary operator that applies an oracle on the target register if the control register state corresponds to a specified positive integer.
ms.openlocfilehash: 6c7f46c44f2a2427f702e463195f26660cb4fca1
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840786"
---
# <a name="controlledonint-function"></a><span data-ttu-id="e4ae8-102">Controlledonint-Funktion</span><span class="sxs-lookup"><span data-stu-id="e4ae8-102">ControlledOnInt function</span></span>

<span data-ttu-id="e4ae8-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="e4ae8-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="e4ae8-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="e4ae8-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="e4ae8-105">Gibt einen einheitlichen Operator zurück, der ein Oracle auf das Ziel Register anwendet, wenn der Steuerelement Registrierungs Zustand einer angegebenen positiven ganzen Zahl entspricht.</span><span class="sxs-lookup"><span data-stu-id="e4ae8-105">Returns a unitary operator that applies an oracle on the target register if the control register state corresponds to a specified positive integer.</span></span>

```qsharp
function ControlledOnInt<'T> (numberState : Int, oracle : ('T => Unit is Adj + Ctl)) : ((Qubit[], 'T) => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="e4ae8-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e4ae8-106">Input</span></span>

### <a name="numberstate--int"></a><span data-ttu-id="e4ae8-107">numstate: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="e4ae8-107">numberState : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="e4ae8-108">Positive Ganzzahl.</span><span class="sxs-lookup"><span data-stu-id="e4ae8-108">Positive integer.</span></span>


### <a name="oracle--t--unit--is-adj--ctl"></a><span data-ttu-id="e4ae8-109">Oracle: 't => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="e4ae8-109">oracle : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="e4ae8-110">Einheitlicher Operator.</span><span class="sxs-lookup"><span data-stu-id="e4ae8-110">Unitary operator.</span></span>



## <a name="output--qubitt--unit--is-adj--ctl"></a><span data-ttu-id="e4ae8-111">Ausgabe: ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[], 't) => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="e4ae8-111">Output : ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[],'T) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="e4ae8-112">Ein einheitlicher Operator, `oracle` der auf das Ziel Register angewendet wird, wenn der Registrierungs Zustand des Steuer Elements dem Zahlen Zustand entspricht `numberState` .</span><span class="sxs-lookup"><span data-stu-id="e4ae8-112">A unitary operator that applies `oracle` on the target register if the control register state corresponds to the number state `numberState`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="e4ae8-113">Typparameter</span><span class="sxs-lookup"><span data-stu-id="e4ae8-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="e4ae8-114">GIF</span><span class="sxs-lookup"><span data-stu-id="e4ae8-114">'T</span></span>



## <a name="remarks"></a><span data-ttu-id="e4ae8-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e4ae8-115">Remarks</span></span>

<span data-ttu-id="e4ae8-116">Der Wert von `numberState` wird mithilfe einer Little-enumdian-Codierung interpretiert.</span><span class="sxs-lookup"><span data-stu-id="e4ae8-116">The value of `numberState` is interpreted using a little-endian encoding.</span></span>