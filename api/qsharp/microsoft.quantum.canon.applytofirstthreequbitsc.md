---
uid: Microsoft.Quantum.Canon.ApplyToFirstThreeQubitsC
title: Applydefirstthreequbitsc-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToFirstThreeQubitsC
qsharp.summary: Applies an operation to the first three qubits in the register. The modifier `C` indicates that the operation is controllable.
ms.openlocfilehash: 2c4fe7c645913cb0703982d78f65645f141fdcae
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841407"
---
# <a name="applytofirstthreequbitsc-operation"></a><span data-ttu-id="a11e5-102">Applydefirstthreequbitsc-Vorgang</span><span class="sxs-lookup"><span data-stu-id="a11e5-102">ApplyToFirstThreeQubitsC operation</span></span>

<span data-ttu-id="a11e5-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="a11e5-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="a11e5-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a11e5-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="a11e5-105">Wendet einen Vorgang auf die ersten drei Qubits im Register an.</span><span class="sxs-lookup"><span data-stu-id="a11e5-105">Applies an operation to the first three qubits in the register.</span></span>
<span data-ttu-id="a11e5-106">Der-Modifizierer `C` gibt an, dass der Vorgang steuerbar ist.</span><span class="sxs-lookup"><span data-stu-id="a11e5-106">The modifier `C` indicates that the operation is controllable.</span></span>

```qsharp
operation ApplyToFirstThreeQubitsC (op : ((Qubit, Qubit, Qubit) => Unit is Ctl), register : Qubit[]) : Unit is Ctl
```


## <a name="input"></a><span data-ttu-id="a11e5-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a11e5-107">Input</span></span>

### <a name="op--qubitqubitqubit--unit--is-ctl"></a><span data-ttu-id="a11e5-108">OP: ([Qubit](xref:microsoft.quantum.lang-ref.qubit),[Qubit](xref:microsoft.quantum.lang-ref.qubit),[Qubit](xref:microsoft.quantum.lang-ref.qubit)) => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist CTL</span><span class="sxs-lookup"><span data-stu-id="a11e5-108">op : ([Qubit](xref:microsoft.quantum.lang-ref.qubit),[Qubit](xref:microsoft.quantum.lang-ref.qubit),[Qubit](xref:microsoft.quantum.lang-ref.qubit)) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="a11e5-109">Ein Vorgang, der auf die ersten drei Qubits angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a11e5-109">An operation to be applied to the first three qubits</span></span>


### <a name="register--qubit"></a><span data-ttu-id="a11e5-110">Register: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="a11e5-110">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="a11e5-111">Qubit-Array mit den ersten drei Qubits, auf die der Vorgang angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="a11e5-111">Qubit array to the first three qubits of which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="a11e5-112">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="a11e5-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="a11e5-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a11e5-113">Remarks</span></span>

<span data-ttu-id="a11e5-114">Das entspricht:</span><span class="sxs-lookup"><span data-stu-id="a11e5-114">This is equivalent to:</span></span>

```qsharp
op(register[0], register[1], register[2]);
```

## <a name="see-also"></a><span data-ttu-id="a11e5-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="a11e5-115">See Also</span></span>

- [<span data-ttu-id="a11e5-116">Microsoft. Quantum. Canon. applyyfirstthreequbits</span><span class="sxs-lookup"><span data-stu-id="a11e5-116">Microsoft.Quantum.Canon.ApplyToFirstThreeQubits</span></span>](xref:Microsoft.Quantum.Canon.ApplyToFirstThreeQubits)