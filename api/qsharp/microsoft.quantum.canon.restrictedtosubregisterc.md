---
uid: Microsoft.Quantum.Canon.RestrictedToSubregisterC
title: Restrictedto subregisterc-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: RestrictedToSubregisterC
qsharp.summary: Restricts an operation to an array of indices of a register, i.e., a subregister. The modifier `C` indicates that the operation is controllable.
ms.openlocfilehash: 2ca32cf8c85f33f498a30f71833b3dd69db6da6e
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703842"
---
# <a name="restrictedtosubregisterc-function"></a><span data-ttu-id="8efa1-102">Restrictedto subregisterc-Funktion</span><span class="sxs-lookup"><span data-stu-id="8efa1-102">RestrictedToSubregisterC function</span></span>

<span data-ttu-id="8efa1-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="8efa1-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="8efa1-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="8efa1-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="8efa1-105">Schränkt einen Vorgang auf ein Array von Indizes eines Registers ein, d. h. ein unter Register.</span><span class="sxs-lookup"><span data-stu-id="8efa1-105">Restricts an operation to an array of indices of a register, i.e., a subregister.</span></span>
<span data-ttu-id="8efa1-106">Der-Modifizierer `C` gibt an, dass der Vorgang steuerbar ist.</span><span class="sxs-lookup"><span data-stu-id="8efa1-106">The modifier `C` indicates that the operation is controllable.</span></span>

```qsharp
function RestrictedToSubregisterC (op : (Qubit[] => Unit is Ctl), idxs : Int[]) : (Qubit[] => Unit is Ctl)
```


## <a name="input"></a><span data-ttu-id="8efa1-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8efa1-107">Input</span></span>

### <a name="op--qubit--unit-ctl"></a><span data-ttu-id="8efa1-108">OP: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) CTL</span><span class="sxs-lookup"><span data-stu-id="8efa1-108">op : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>

<span data-ttu-id="8efa1-109">Der Vorgang, der auf ein unter Register beschränkt werden soll.</span><span class="sxs-lookup"><span data-stu-id="8efa1-109">Operation to be restricted to a subregister.</span></span>


### <a name="idxs--int"></a><span data-ttu-id="8efa1-110">idxs: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="8efa1-110">idxs : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="8efa1-111">Ein Array von Indizes, das angibt, auf welche Qubits der Vorgang beschränkt wird.</span><span class="sxs-lookup"><span data-stu-id="8efa1-111">Array of indices, indicating to which qubits the operation will be restricted.</span></span>



## <a name="output--qubit--unit-ctl"></a><span data-ttu-id="8efa1-112">Ausgabe: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) CTL</span><span class="sxs-lookup"><span data-stu-id="8efa1-112">Output : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>



## <a name="see-also"></a><span data-ttu-id="8efa1-113">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="8efa1-113">See Also</span></span>

- [<span data-ttu-id="8efa1-114">Microsoft. Quantum. Canon. restricteddesubregister</span><span class="sxs-lookup"><span data-stu-id="8efa1-114">Microsoft.Quantum.Canon.RestrictedToSubregister</span></span>](xref:Microsoft.Quantum.Canon.RestrictedToSubregister)