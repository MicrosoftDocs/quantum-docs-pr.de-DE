---
uid: Microsoft.Quantum.Canon.ApplyToSubregister
title: Applydesubregister-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToSubregister
qsharp.summary: Applies an operation to a subregister of a register, with qubits specified by an array of their indices.
ms.openlocfilehash: c9181b8962d36b20f7a9140eb7aaef11aee7faa0
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704663"
---
# <a name="applytosubregister-operation"></a><span data-ttu-id="abf7d-102">Applydesubregister-Vorgang</span><span class="sxs-lookup"><span data-stu-id="abf7d-102">ApplyToSubregister operation</span></span>

<span data-ttu-id="abf7d-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="abf7d-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="abf7d-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="abf7d-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="abf7d-105">Wendet einen Vorgang auf ein unter Register eines Register mit Qubits an, die durch ein Array ihrer Indizes angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="abf7d-105">Applies an operation to a subregister of a register, with qubits specified by an array of their indices.</span></span>

```qsharp
operation ApplyToSubregister (op : (Qubit[] => Unit), idxs : Int[], target : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="abf7d-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="abf7d-106">Input</span></span>

### <a name="op--qubit--unit"></a><span data-ttu-id="abf7d-107">OP: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="abf7d-107">op : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="abf7d-108">Der für die unter Registrierung anzuwendende Vorgang.</span><span class="sxs-lookup"><span data-stu-id="abf7d-108">Operation to apply to subregister.</span></span>


### <a name="idxs--int"></a><span data-ttu-id="abf7d-109">idxs: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="abf7d-109">idxs : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="abf7d-110">Ein Array von Indizes, das angibt, auf welche Qubits der Vorgang angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="abf7d-110">Array of indices, indicating to which qubits the operation will be applied.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="abf7d-111">Ziel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="abf7d-111">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="abf7d-112">Registrieren Sie sich für den Vorgang.</span><span class="sxs-lookup"><span data-stu-id="abf7d-112">Register on which the operation acts.</span></span>



## <a name="output--unit"></a><span data-ttu-id="abf7d-113">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="abf7d-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="abf7d-114">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="abf7d-114">See Also</span></span>

- [<span data-ttu-id="abf7d-115">Microsoft. Quantum. Canon. ApplyTo subregistera</span><span class="sxs-lookup"><span data-stu-id="abf7d-115">Microsoft.Quantum.Canon.ApplyToSubregisterA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToSubregisterA)
- [<span data-ttu-id="abf7d-116">Microsoft. Quantum. Canon. ApplyTo subregisterc</span><span class="sxs-lookup"><span data-stu-id="abf7d-116">Microsoft.Quantum.Canon.ApplyToSubregisterC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToSubregisterC)
- [<span data-ttu-id="abf7d-117">Microsoft. Quantum. Canon. ApplyTo subregisterca</span><span class="sxs-lookup"><span data-stu-id="abf7d-117">Microsoft.Quantum.Canon.ApplyToSubregisterCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToSubregisterCA)