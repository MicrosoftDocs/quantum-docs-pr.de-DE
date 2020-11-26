---
uid: Microsoft.Quantum.Canon.ApplyToFirstThreeQubitsCA
title: Applydefirstthreequbitsca-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToFirstThreeQubitsCA
qsharp.summary: Applies an operation to the first three qubits in the register. The modifier `CA` indicates that the operation is controllable and adjointable.
ms.openlocfilehash: 7e090a116a63e26278b05dc7c2fda9b65ff15bae
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96208787"
---
# <a name="applytofirstthreequbitsca-operation"></a><span data-ttu-id="0951e-102">Applydefirstthreequbitsca-Vorgang</span><span class="sxs-lookup"><span data-stu-id="0951e-102">ApplyToFirstThreeQubitsCA operation</span></span>

<span data-ttu-id="0951e-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="0951e-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="0951e-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="0951e-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="0951e-105">Wendet einen Vorgang auf die ersten drei Qubits im Register an.</span><span class="sxs-lookup"><span data-stu-id="0951e-105">Applies an operation to the first three qubits in the register.</span></span>
<span data-ttu-id="0951e-106">Der-Modifizierer `CA` gibt an, dass der Vorgang steuerbar und adjointable ist.</span><span class="sxs-lookup"><span data-stu-id="0951e-106">The modifier `CA` indicates that the operation is controllable and adjointable.</span></span>

```qsharp
operation ApplyToFirstThreeQubitsCA (op : ((Qubit, Qubit, Qubit) => Unit is Adj + Ctl), register : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="0951e-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0951e-107">Input</span></span>

### <a name="op--qubitqubitqubit--unit--is-adj--ctl"></a><span data-ttu-id="0951e-108">OP: ([Qubit](xref:microsoft.quantum.lang-ref.qubit),[Qubit](xref:microsoft.quantum.lang-ref.qubit),[Qubit](xref:microsoft.quantum.lang-ref.qubit)) => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="0951e-108">op : ([Qubit](xref:microsoft.quantum.lang-ref.qubit),[Qubit](xref:microsoft.quantum.lang-ref.qubit),[Qubit](xref:microsoft.quantum.lang-ref.qubit)) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="0951e-109">Ein Vorgang, der auf die ersten drei Qubits angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="0951e-109">An operation to be applied to the first three qubits</span></span>


### <a name="register--qubit"></a><span data-ttu-id="0951e-110">Register: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="0951e-110">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="0951e-111">Qubit-Array mit den ersten drei Qubits, auf die der Vorgang angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="0951e-111">Qubit array to the first three qubits of which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="0951e-112">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="0951e-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="0951e-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0951e-113">Remarks</span></span>

<span data-ttu-id="0951e-114">Das entspricht:</span><span class="sxs-lookup"><span data-stu-id="0951e-114">This is equivalent to:</span></span>

```qsharp
op(register[0], register[1], register[2]);
```

## <a name="see-also"></a><span data-ttu-id="0951e-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="0951e-115">See Also</span></span>

- [<span data-ttu-id="0951e-116">Microsoft. Quantum. Canon. applyyfirstthreequbits</span><span class="sxs-lookup"><span data-stu-id="0951e-116">Microsoft.Quantum.Canon.ApplyToFirstThreeQubits</span></span>](xref:Microsoft.Quantum.Canon.ApplyToFirstThreeQubits)