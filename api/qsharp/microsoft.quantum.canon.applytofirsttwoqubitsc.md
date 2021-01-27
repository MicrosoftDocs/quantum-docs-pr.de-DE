---
uid: Microsoft.Quantum.Canon.ApplyToFirstTwoQubitsC
title: Applydefirsttwoqubitsc-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToFirstTwoQubitsC
qsharp.summary: Applies an operation to the first two qubits in the register. The modifier `C` indicates that the operation is controllable.
ms.openlocfilehash: f71209a806b0d1d712a3c776eb45e62d1cd5d5f7
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841356"
---
# <a name="applytofirsttwoqubitsc-operation"></a><span data-ttu-id="72b24-102">Applydefirsttwoqubitsc-Vorgang</span><span class="sxs-lookup"><span data-stu-id="72b24-102">ApplyToFirstTwoQubitsC operation</span></span>

<span data-ttu-id="72b24-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="72b24-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="72b24-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="72b24-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="72b24-105">Wendet einen Vorgang auf die ersten beiden Qubits im Register an.</span><span class="sxs-lookup"><span data-stu-id="72b24-105">Applies an operation to the first two qubits in the register.</span></span>
<span data-ttu-id="72b24-106">Der-Modifizierer `C` gibt an, dass der Vorgang steuerbar ist.</span><span class="sxs-lookup"><span data-stu-id="72b24-106">The modifier `C` indicates that the operation is controllable.</span></span>

```qsharp
operation ApplyToFirstTwoQubitsC (op : ((Qubit, Qubit) => Unit is Ctl), register : Qubit[]) : Unit is Ctl
```


## <a name="input"></a><span data-ttu-id="72b24-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="72b24-107">Input</span></span>

### <a name="op--qubitqubit--unit--is-ctl"></a><span data-ttu-id="72b24-108">OP: ([Qubit](xref:microsoft.quantum.lang-ref.qubit),[Qubit](xref:microsoft.quantum.lang-ref.qubit)) => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist CTL</span><span class="sxs-lookup"><span data-stu-id="72b24-108">op : ([Qubit](xref:microsoft.quantum.lang-ref.qubit),[Qubit](xref:microsoft.quantum.lang-ref.qubit)) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="72b24-109">Ein Vorgang, der auf die ersten beiden Qubits angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="72b24-109">An operation to be applied to the first two qubits</span></span>


### <a name="register--qubit"></a><span data-ttu-id="72b24-110">Register: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="72b24-110">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="72b24-111">Qubit-Array zu den ersten zwei Qubits, auf die der Vorgang angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="72b24-111">Qubit array to the first two qubits of which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="72b24-112">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="72b24-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="72b24-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="72b24-113">Remarks</span></span>

<span data-ttu-id="72b24-114">Das entspricht:</span><span class="sxs-lookup"><span data-stu-id="72b24-114">This is equivalent to:</span></span>

```qsharp
op(register[0], register[1]);
```

## <a name="see-also"></a><span data-ttu-id="72b24-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="72b24-115">See Also</span></span>

- [<span data-ttu-id="72b24-116">Microsoft. Quantum. Canon. applyjefirsttwoqubits</span><span class="sxs-lookup"><span data-stu-id="72b24-116">Microsoft.Quantum.Canon.ApplyToFirstTwoQubits</span></span>](xref:Microsoft.Quantum.Canon.ApplyToFirstTwoQubits)