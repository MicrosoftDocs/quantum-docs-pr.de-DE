---
uid: Microsoft.Quantum.Canon.ApplyToFirstThreeQubits
title: Applydefirstthreequbits-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToFirstThreeQubits
qsharp.summary: Applies an operation to the first three qubits in the register.
ms.openlocfilehash: b01c1072306cfdebcb90827a14683a32312481fc
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850700"
---
# <a name="applytofirstthreequbits-operation"></a><span data-ttu-id="7afd1-102">Applydefirstthreequbits-Vorgang</span><span class="sxs-lookup"><span data-stu-id="7afd1-102">ApplyToFirstThreeQubits operation</span></span>

<span data-ttu-id="7afd1-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="7afd1-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="7afd1-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="7afd1-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="7afd1-105">Wendet einen Vorgang auf die ersten drei Qubits im Register an.</span><span class="sxs-lookup"><span data-stu-id="7afd1-105">Applies an operation to the first three qubits in the register.</span></span>

```qsharp
operation ApplyToFirstThreeQubits (op : ((Qubit, Qubit, Qubit) => Unit), register : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="7afd1-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="7afd1-106">Input</span></span>

### <a name="op--qubitqubitqubit--unit"></a><span data-ttu-id="7afd1-107">OP: ([Qubit](xref:microsoft.quantum.lang-ref.qubit),[Qubit](xref:microsoft.quantum.lang-ref.qubit),[Qubit](xref:microsoft.quantum.lang-ref.qubit)) => [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="7afd1-107">op : ([Qubit](xref:microsoft.quantum.lang-ref.qubit),[Qubit](xref:microsoft.quantum.lang-ref.qubit),[Qubit](xref:microsoft.quantum.lang-ref.qubit)) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="7afd1-108">Ein Vorgang, der auf die ersten drei Qubits angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="7afd1-108">An operation to be applied to the first three qubits</span></span>


### <a name="register--qubit"></a><span data-ttu-id="7afd1-109">Register: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="7afd1-109">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="7afd1-110">Qubit-Array mit den ersten drei Qubits, auf die der Vorgang angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="7afd1-110">Qubit array to the first three qubits of which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="7afd1-111">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="7afd1-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="7afd1-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7afd1-112">Remarks</span></span>

<span data-ttu-id="7afd1-113">Das entspricht:</span><span class="sxs-lookup"><span data-stu-id="7afd1-113">This is equivalent to:</span></span>

```qsharp
op(register[0], register[1], register[2]);
```

## <a name="see-also"></a><span data-ttu-id="7afd1-114">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="7afd1-114">See Also</span></span>

- [<span data-ttu-id="7afd1-115">Microsoft. Quantum. Canon. applyyfirstthreequbitsc</span><span class="sxs-lookup"><span data-stu-id="7afd1-115">Microsoft.Quantum.Canon.ApplyToFirstThreeQubitsC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToFirstThreeQubitsC)
- [<span data-ttu-id="7afd1-116">Microsoft. Quantum. Canon. applyyfirstthreequbitsa</span><span class="sxs-lookup"><span data-stu-id="7afd1-116">Microsoft.Quantum.Canon.ApplyToFirstThreeQubitsA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToFirstThreeQubitsA)
- [<span data-ttu-id="7afd1-117">Microsoft. Quantum. Canon. applyyfirstthreequbitsca</span><span class="sxs-lookup"><span data-stu-id="7afd1-117">Microsoft.Quantum.Canon.ApplyToFirstThreeQubitsCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToFirstThreeQubitsCA)