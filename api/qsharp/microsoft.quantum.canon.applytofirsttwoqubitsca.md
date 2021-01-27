---
uid: Microsoft.Quantum.Canon.ApplyToFirstTwoQubitsCA
title: Applydefirsttwoqubitsca-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToFirstTwoQubitsCA
qsharp.summary: Applies an operation to the first two qubits in the register. The modifier `CA` indicates that the operation is controllable and adjointable.
ms.openlocfilehash: 5bea9ec1be1fc379823877684c81e99f86807d89
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850660"
---
# <a name="applytofirsttwoqubitsca-operation"></a><span data-ttu-id="56eea-102">Applydefirsttwoqubitsca-Vorgang</span><span class="sxs-lookup"><span data-stu-id="56eea-102">ApplyToFirstTwoQubitsCA operation</span></span>

<span data-ttu-id="56eea-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="56eea-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="56eea-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="56eea-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="56eea-105">Wendet einen Vorgang auf die ersten beiden Qubits im Register an.</span><span class="sxs-lookup"><span data-stu-id="56eea-105">Applies an operation to the first two qubits in the register.</span></span>
<span data-ttu-id="56eea-106">Der-Modifizierer `CA` gibt an, dass der Vorgang steuerbar und adjointable ist.</span><span class="sxs-lookup"><span data-stu-id="56eea-106">The modifier `CA` indicates that the operation is controllable and adjointable.</span></span>

```qsharp
operation ApplyToFirstTwoQubitsCA (op : ((Qubit, Qubit) => Unit is Adj + Ctl), register : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="56eea-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="56eea-107">Input</span></span>

### <a name="op--qubitqubit--unit--is-adj--ctl"></a><span data-ttu-id="56eea-108">OP: ([Qubit](xref:microsoft.quantum.lang-ref.qubit),[Qubit](xref:microsoft.quantum.lang-ref.qubit)) => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="56eea-108">op : ([Qubit](xref:microsoft.quantum.lang-ref.qubit),[Qubit](xref:microsoft.quantum.lang-ref.qubit)) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="56eea-109">Ein Vorgang, der auf die ersten beiden Qubits angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="56eea-109">An operation to be applied to the first two qubits</span></span>


### <a name="register--qubit"></a><span data-ttu-id="56eea-110">Register: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="56eea-110">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="56eea-111">Qubit-Array zu den ersten zwei Qubits, auf die der Vorgang angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="56eea-111">Qubit array to the first two qubits of which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="56eea-112">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="56eea-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="56eea-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="56eea-113">Remarks</span></span>

<span data-ttu-id="56eea-114">Das entspricht:</span><span class="sxs-lookup"><span data-stu-id="56eea-114">This is equivalent to:</span></span>

```qsharp
op(register[0], register[1]);
```

## <a name="see-also"></a><span data-ttu-id="56eea-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="56eea-115">See Also</span></span>

- [<span data-ttu-id="56eea-116">Microsoft. Quantum. Canon. applyjefirsttwoqubits</span><span class="sxs-lookup"><span data-stu-id="56eea-116">Microsoft.Quantum.Canon.ApplyToFirstTwoQubits</span></span>](xref:Microsoft.Quantum.Canon.ApplyToFirstTwoQubits)