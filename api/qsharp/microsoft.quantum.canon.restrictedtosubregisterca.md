---
uid: Microsoft.Quantum.Canon.RestrictedToSubregisterCA
title: Restricteddesubregisterca-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: RestrictedToSubregisterCA
qsharp.summary: Restricts an operation to an array of indices of a register, i.e., a subregister. The modifier `CA` indicates that the operation is controllable and adjointable.
ms.openlocfilehash: e81193a85451b72a69a595fa81a9fb07f3038c22
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703848"
---
# <a name="restrictedtosubregisterca-function"></a><span data-ttu-id="2a33f-102">Restricteddesubregisterca-Funktion</span><span class="sxs-lookup"><span data-stu-id="2a33f-102">RestrictedToSubregisterCA function</span></span>

<span data-ttu-id="2a33f-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="2a33f-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="2a33f-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="2a33f-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="2a33f-105">Schränkt einen Vorgang auf ein Array von Indizes eines Registers ein, d. h. ein unter Register.</span><span class="sxs-lookup"><span data-stu-id="2a33f-105">Restricts an operation to an array of indices of a register, i.e., a subregister.</span></span>
<span data-ttu-id="2a33f-106">Der-Modifizierer `CA` gibt an, dass der Vorgang steuerbar und adjointable ist.</span><span class="sxs-lookup"><span data-stu-id="2a33f-106">The modifier `CA` indicates that the operation is controllable and adjointable.</span></span>

```qsharp
function RestrictedToSubregisterCA (op : (Qubit[] => Unit is Adj + Ctl), idxs : Int[]) : (Qubit[] => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="2a33f-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2a33f-107">Input</span></span>

### <a name="op--qubit--unit-adj--ctl"></a><span data-ttu-id="2a33f-108">OP: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="2a33f-108">op : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="2a33f-109">Der Vorgang, der auf ein unter Register beschränkt werden soll.</span><span class="sxs-lookup"><span data-stu-id="2a33f-109">Operation to be restricted to a subregister.</span></span>


### <a name="idxs--int"></a><span data-ttu-id="2a33f-110">idxs: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="2a33f-110">idxs : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="2a33f-111">Ein Array von Indizes, das angibt, auf welche Qubits der Vorgang beschränkt wird.</span><span class="sxs-lookup"><span data-stu-id="2a33f-111">Array of indices, indicating to which qubits the operation will be restricted.</span></span>



## <a name="output--qubit--unit-adj--ctl"></a><span data-ttu-id="2a33f-112">Ausgabe: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="2a33f-112">Output : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>



## <a name="see-also"></a><span data-ttu-id="2a33f-113">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="2a33f-113">See Also</span></span>

- [<span data-ttu-id="2a33f-114">Microsoft. Quantum. Canon. restricteddesubregister</span><span class="sxs-lookup"><span data-stu-id="2a33f-114">Microsoft.Quantum.Canon.RestrictedToSubregister</span></span>](xref:Microsoft.Quantum.Canon.RestrictedToSubregister)