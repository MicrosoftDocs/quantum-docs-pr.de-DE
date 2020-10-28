---
uid: Microsoft.Quantum.Canon.ApplyToSubregisterCA
title: Applydesubregisterca-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToSubregisterCA
qsharp.summary: Applies an operation to a subregister of a register, with qubits specified by an array of their indices. The modifier `CA` indicates that the operation is controllable and adjointable.
ms.openlocfilehash: 3eb210debf8980f057ed150f647d545f68734459
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704639"
---
# <a name="applytosubregisterca-operation"></a><span data-ttu-id="fbec9-102">Applydesubregisterca-Vorgang</span><span class="sxs-lookup"><span data-stu-id="fbec9-102">ApplyToSubregisterCA operation</span></span>

<span data-ttu-id="fbec9-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="fbec9-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="fbec9-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="fbec9-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="fbec9-105">Wendet einen Vorgang auf ein unter Register eines Register mit Qubits an, die durch ein Array ihrer Indizes angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="fbec9-105">Applies an operation to a subregister of a register, with qubits specified by an array of their indices.</span></span>
<span data-ttu-id="fbec9-106">Der-Modifizierer `CA` gibt an, dass der Vorgang steuerbar und adjointable ist.</span><span class="sxs-lookup"><span data-stu-id="fbec9-106">The modifier `CA` indicates that the operation is controllable and adjointable.</span></span>

```qsharp
operation ApplyToSubregisterCA (op : (Qubit[] => Unit is Ctl + Adj), idxs : Int[], target : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="fbec9-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="fbec9-107">Input</span></span>

### <a name="op--qubit--unit-ctl--adj"></a><span data-ttu-id="fbec9-108">OP: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) CTL + ADJ</span><span class="sxs-lookup"><span data-stu-id="fbec9-108">op : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl + Adj</span></span>

<span data-ttu-id="fbec9-109">Der für die unter Registrierung anzuwendende Vorgang.</span><span class="sxs-lookup"><span data-stu-id="fbec9-109">Operation to apply to subregister.</span></span>


### <a name="idxs--int"></a><span data-ttu-id="fbec9-110">idxs: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="fbec9-110">idxs : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="fbec9-111">Ein Array von Indizes, das angibt, auf welche Qubits der Vorgang angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="fbec9-111">Array of indices, indicating to which qubits the operation will be applied.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="fbec9-112">Ziel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="fbec9-112">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="fbec9-113">Registrieren Sie sich für den Vorgang.</span><span class="sxs-lookup"><span data-stu-id="fbec9-113">Register on which the operation acts.</span></span>



## <a name="output--unit"></a><span data-ttu-id="fbec9-114">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="fbec9-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="fbec9-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="fbec9-115">See Also</span></span>

- [<span data-ttu-id="fbec9-116">Microsoft. Quantum. Canon. applydesubregister</span><span class="sxs-lookup"><span data-stu-id="fbec9-116">Microsoft.Quantum.Canon.ApplyToSubregister</span></span>](xref:Microsoft.Quantum.Canon.ApplyToSubregister)