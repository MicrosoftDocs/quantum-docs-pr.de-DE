---
uid: Microsoft.Quantum.Canon.ApplyToSubregisterA
title: Applydesubregistera-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToSubregisterA
qsharp.summary: Applies an operation to a subregister of a register, with qubits specified by an array of their indices. The modifier `A` indicates that the operation is adjointable.
ms.openlocfilehash: e0c546b768320ce43e7b44242d15838194e1089d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704658"
---
# <a name="applytosubregistera-operation"></a><span data-ttu-id="d195c-102">Applydesubregistera-Vorgang</span><span class="sxs-lookup"><span data-stu-id="d195c-102">ApplyToSubregisterA operation</span></span>

<span data-ttu-id="d195c-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="d195c-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="d195c-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="d195c-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="d195c-105">Wendet einen Vorgang auf ein unter Register eines Register mit Qubits an, die durch ein Array ihrer Indizes angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="d195c-105">Applies an operation to a subregister of a register, with qubits specified by an array of their indices.</span></span>
<span data-ttu-id="d195c-106">Der-Modifizierer `A` gibt an, dass der Vorgang adjointable ist.</span><span class="sxs-lookup"><span data-stu-id="d195c-106">The modifier `A` indicates that the operation is adjointable.</span></span>

```qsharp
operation ApplyToSubregisterA (op : (Qubit[] => Unit is Adj), idxs : Int[], target : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="d195c-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d195c-107">Input</span></span>

### <a name="op--qubit--unit-adj"></a><span data-ttu-id="d195c-108">OP: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ</span><span class="sxs-lookup"><span data-stu-id="d195c-108">op : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="d195c-109">Der für die unter Registrierung anzuwendende Vorgang.</span><span class="sxs-lookup"><span data-stu-id="d195c-109">Operation to apply to subregister.</span></span>


### <a name="idxs--int"></a><span data-ttu-id="d195c-110">idxs: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="d195c-110">idxs : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="d195c-111">Ein Array von Indizes, das angibt, auf welche Qubits der Vorgang angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="d195c-111">Array of indices, indicating to which qubits the operation will be applied.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="d195c-112">Ziel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="d195c-112">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="d195c-113">Registrieren Sie sich für den Vorgang.</span><span class="sxs-lookup"><span data-stu-id="d195c-113">Register on which the operation acts.</span></span>



## <a name="output--unit"></a><span data-ttu-id="d195c-114">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="d195c-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="d195c-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="d195c-115">See Also</span></span>

- [<span data-ttu-id="d195c-116">Microsoft. Quantum. Canon. applydesubregister</span><span class="sxs-lookup"><span data-stu-id="d195c-116">Microsoft.Quantum.Canon.ApplyToSubregister</span></span>](xref:Microsoft.Quantum.Canon.ApplyToSubregister)