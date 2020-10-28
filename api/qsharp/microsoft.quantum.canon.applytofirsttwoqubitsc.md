---
uid: Microsoft.Quantum.Canon.ApplyToFirstTwoQubitsC
title: Applydefirsttwoqubitsc-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToFirstTwoQubitsC
qsharp.summary: Applies an operation to the first two qubits in the register. The modifier `C` indicates that the operation is controllable.
ms.openlocfilehash: 97706ffcc8700a0055ff37bbbaccc6fb4f8854b6
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704807"
---
# <a name="applytofirsttwoqubitsc-operation"></a><span data-ttu-id="f1ef3-102">Applydefirsttwoqubitsc-Vorgang</span><span class="sxs-lookup"><span data-stu-id="f1ef3-102">ApplyToFirstTwoQubitsC operation</span></span>

<span data-ttu-id="f1ef3-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="f1ef3-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="f1ef3-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="f1ef3-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="f1ef3-105">Wendet einen Vorgang auf die ersten beiden Qubits im Register an.</span><span class="sxs-lookup"><span data-stu-id="f1ef3-105">Applies an operation to the first two qubits in the register.</span></span>
<span data-ttu-id="f1ef3-106">Der-Modifizierer `C` gibt an, dass der Vorgang steuerbar ist.</span><span class="sxs-lookup"><span data-stu-id="f1ef3-106">The modifier `C` indicates that the operation is controllable.</span></span>

```qsharp
operation ApplyToFirstTwoQubitsC (op : ((Qubit, Qubit) => Unit is Ctl), register : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="f1ef3-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f1ef3-107">Input</span></span>

### <a name="op--qubitqubit--unit-ctl"></a><span data-ttu-id="f1ef3-108">OP: ([Qubit](xref:microsoft.quantum.lang-ref.qubit),[Qubit](xref:microsoft.quantum.lang-ref.qubit)) => [Unit](xref:microsoft.quantum.lang-ref.unit) CTL</span><span class="sxs-lookup"><span data-stu-id="f1ef3-108">op : ([Qubit](xref:microsoft.quantum.lang-ref.qubit),[Qubit](xref:microsoft.quantum.lang-ref.qubit)) => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>

<span data-ttu-id="f1ef3-109">Ein Vorgang, der auf die ersten beiden Qubits angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f1ef3-109">An operation to be applied to the first two qubits</span></span>


### <a name="register--qubit"></a><span data-ttu-id="f1ef3-110">Register: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="f1ef3-110">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="f1ef3-111">Qubit-Array zu den ersten zwei Qubits, auf die der Vorgang angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="f1ef3-111">Qubit array to the first two qubits of which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="f1ef3-112">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="f1ef3-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="f1ef3-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f1ef3-113">Remarks</span></span>

<span data-ttu-id="f1ef3-114">Das entspricht:</span><span class="sxs-lookup"><span data-stu-id="f1ef3-114">This is equivalent to:</span></span>

```qsharp
op(register[0], register[1]);
```

## <a name="see-also"></a><span data-ttu-id="f1ef3-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="f1ef3-115">See Also</span></span>

- [<span data-ttu-id="f1ef3-116">Microsoft. Quantum. Canon. applyjefirsttwoqubits</span><span class="sxs-lookup"><span data-stu-id="f1ef3-116">Microsoft.Quantum.Canon.ApplyToFirstTwoQubits</span></span>](xref:Microsoft.Quantum.Canon.ApplyToFirstTwoQubits)