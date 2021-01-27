---
uid: Microsoft.Quantum.Canon.ApplyToFirstTwoQubitsA
title: Applydefirsttwoqubitsa-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToFirstTwoQubitsA
qsharp.summary: Applies an operation to the first two qubits in the register. The modifier `A` indicates that the operation is adjointable.
ms.openlocfilehash: 197f1da6682b100a0b71f3548727188c0ef6f7c3
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850675"
---
# <a name="applytofirsttwoqubitsa-operation"></a><span data-ttu-id="8fea4-102">Applydefirsttwoqubitsa-Vorgang</span><span class="sxs-lookup"><span data-stu-id="8fea4-102">ApplyToFirstTwoQubitsA operation</span></span>

<span data-ttu-id="8fea4-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="8fea4-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="8fea4-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="8fea4-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="8fea4-105">Wendet einen Vorgang auf die ersten beiden Qubits im Register an.</span><span class="sxs-lookup"><span data-stu-id="8fea4-105">Applies an operation to the first two qubits in the register.</span></span>
<span data-ttu-id="8fea4-106">Der-Modifizierer `A` gibt an, dass der Vorgang adjointable ist.</span><span class="sxs-lookup"><span data-stu-id="8fea4-106">The modifier `A` indicates that the operation is adjointable.</span></span>

```qsharp
operation ApplyToFirstTwoQubitsA (op : ((Qubit, Qubit) => Unit is Adj), register : Qubit[]) : Unit is Adj
```


## <a name="input"></a><span data-ttu-id="8fea4-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8fea4-107">Input</span></span>

### <a name="op--qubitqubit--unit--is-adj"></a><span data-ttu-id="8fea4-108">OP: ([Qubit](xref:microsoft.quantum.lang-ref.qubit),[Qubit](xref:microsoft.quantum.lang-ref.qubit)) => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ</span><span class="sxs-lookup"><span data-stu-id="8fea4-108">op : ([Qubit](xref:microsoft.quantum.lang-ref.qubit),[Qubit](xref:microsoft.quantum.lang-ref.qubit)) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="8fea4-109">Ein Vorgang, der auf die ersten beiden Qubits angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="8fea4-109">An operation to be applied to the first two qubits</span></span>


### <a name="register--qubit"></a><span data-ttu-id="8fea4-110">Register: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="8fea4-110">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="8fea4-111">Qubit-Array zu den ersten zwei Qubits, auf die der Vorgang angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="8fea4-111">Qubit array to the first two qubits of which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="8fea4-112">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="8fea4-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="8fea4-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8fea4-113">Remarks</span></span>

<span data-ttu-id="8fea4-114">Das entspricht:</span><span class="sxs-lookup"><span data-stu-id="8fea4-114">This is equivalent to:</span></span>

```qsharp
op(register[0], register[1]);
```

## <a name="see-also"></a><span data-ttu-id="8fea4-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="8fea4-115">See Also</span></span>

- [<span data-ttu-id="8fea4-116">Microsoft. Quantum. Canon. applyjefirsttwoqubits</span><span class="sxs-lookup"><span data-stu-id="8fea4-116">Microsoft.Quantum.Canon.ApplyToFirstTwoQubits</span></span>](xref:Microsoft.Quantum.Canon.ApplyToFirstTwoQubits)