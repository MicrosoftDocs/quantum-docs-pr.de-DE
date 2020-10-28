---
uid: Microsoft.Quantum.Canon.RestrictedToSubregisterA
title: Restricteddesubregistera-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: RestrictedToSubregisterA
qsharp.summary: Restricts an operation to an array of indices of a register, i.e., a subregister. The modifier `A` indicates that the operation is adjointable.
ms.openlocfilehash: d45c43caed35df8fb89d9d38e540faf5a21ea064
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703853"
---
# <a name="restrictedtosubregistera-function"></a><span data-ttu-id="0243a-102">Restricteddesubregistera-Funktion</span><span class="sxs-lookup"><span data-stu-id="0243a-102">RestrictedToSubregisterA function</span></span>

<span data-ttu-id="0243a-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="0243a-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="0243a-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="0243a-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="0243a-105">Schränkt einen Vorgang auf ein Array von Indizes eines Registers ein, d. h. ein unter Register.</span><span class="sxs-lookup"><span data-stu-id="0243a-105">Restricts an operation to an array of indices of a register, i.e., a subregister.</span></span>
<span data-ttu-id="0243a-106">Der-Modifizierer `A` gibt an, dass der Vorgang adjointable ist.</span><span class="sxs-lookup"><span data-stu-id="0243a-106">The modifier `A` indicates that the operation is adjointable.</span></span>

```qsharp
function RestrictedToSubregisterA (op : (Qubit[] => Unit is Adj), idxs : Int[]) : (Qubit[] => Unit is Adj)
```


## <a name="input"></a><span data-ttu-id="0243a-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0243a-107">Input</span></span>

### <a name="op--qubit--unit-adj"></a><span data-ttu-id="0243a-108">OP: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ</span><span class="sxs-lookup"><span data-stu-id="0243a-108">op : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="0243a-109">Der Vorgang, der auf ein unter Register beschränkt werden soll.</span><span class="sxs-lookup"><span data-stu-id="0243a-109">Operation to be restricted to a subregister.</span></span>


### <a name="idxs--int"></a><span data-ttu-id="0243a-110">idxs: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="0243a-110">idxs : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="0243a-111">Ein Array von Indizes, das angibt, auf welche Qubits der Vorgang beschränkt wird.</span><span class="sxs-lookup"><span data-stu-id="0243a-111">Array of indices, indicating to which qubits the operation will be restricted.</span></span>



## <a name="output--qubit--unit-adj"></a><span data-ttu-id="0243a-112">Ausgabe: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ</span><span class="sxs-lookup"><span data-stu-id="0243a-112">Output : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>



## <a name="see-also"></a><span data-ttu-id="0243a-113">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="0243a-113">See Also</span></span>

- [<span data-ttu-id="0243a-114">Microsoft. Quantum. Canon. restricteddesubregister</span><span class="sxs-lookup"><span data-stu-id="0243a-114">Microsoft.Quantum.Canon.RestrictedToSubregister</span></span>](xref:Microsoft.Quantum.Canon.RestrictedToSubregister)