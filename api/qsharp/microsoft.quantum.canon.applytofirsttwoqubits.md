---
uid: Microsoft.Quantum.Canon.ApplyToFirstTwoQubits
title: Applydefirsttwoqubits-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToFirstTwoQubits
qsharp.summary: Applies an operation to the first two qubits in the register.
ms.openlocfilehash: aad07889c0dbf2329304c98b06dbd0c225df8a81
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704823"
---
# <a name="applytofirsttwoqubits-operation"></a><span data-ttu-id="12459-102">Applydefirsttwoqubits-Vorgang</span><span class="sxs-lookup"><span data-stu-id="12459-102">ApplyToFirstTwoQubits operation</span></span>

<span data-ttu-id="12459-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="12459-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="12459-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="12459-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="12459-105">Wendet einen Vorgang auf die ersten beiden Qubits im Register an.</span><span class="sxs-lookup"><span data-stu-id="12459-105">Applies an operation to the first two qubits in the register.</span></span>

```qsharp
operation ApplyToFirstTwoQubits (op : ((Qubit, Qubit) => Unit), register : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="12459-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="12459-106">Input</span></span>

### <a name="op--qubitqubit--unit"></a><span data-ttu-id="12459-107">OP: ([Qubit](xref:microsoft.quantum.lang-ref.qubit),[Qubit](xref:microsoft.quantum.lang-ref.qubit)) => [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="12459-107">op : ([Qubit](xref:microsoft.quantum.lang-ref.qubit),[Qubit](xref:microsoft.quantum.lang-ref.qubit)) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="12459-108">Ein Vorgang, der auf die ersten beiden Qubits angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="12459-108">An operation to be applied to the first two qubits</span></span>


### <a name="register--qubit"></a><span data-ttu-id="12459-109">Register: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="12459-109">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="12459-110">Qubit-Array zu den ersten zwei Qubits, auf die der Vorgang angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="12459-110">Qubit array to the first two qubits of which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="12459-111">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="12459-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="12459-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="12459-112">Remarks</span></span>

<span data-ttu-id="12459-113">Das entspricht:</span><span class="sxs-lookup"><span data-stu-id="12459-113">This is equivalent to:</span></span>

```qsharp
op(register[0], register[1]);
```

## <a name="see-also"></a><span data-ttu-id="12459-114">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="12459-114">See Also</span></span>

- [<span data-ttu-id="12459-115">Microsoft. Quantum. Canon. applyjefirsttwoqubitsa</span><span class="sxs-lookup"><span data-stu-id="12459-115">Microsoft.Quantum.Canon.ApplyToFirstTwoQubitsA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToFirstTwoQubitsA)
- [<span data-ttu-id="12459-116">Microsoft. Quantum. Canon. applyjefirsttwoqubitsc</span><span class="sxs-lookup"><span data-stu-id="12459-116">Microsoft.Quantum.Canon.ApplyToFirstTwoQubitsC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToFirstTwoQubitsC)
- [<span data-ttu-id="12459-117">Microsoft. Quantum. Canon. applyyfirsttwoqubitsca</span><span class="sxs-lookup"><span data-stu-id="12459-117">Microsoft.Quantum.Canon.ApplyToFirstTwoQubitsCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToFirstTwoQubitsCA)