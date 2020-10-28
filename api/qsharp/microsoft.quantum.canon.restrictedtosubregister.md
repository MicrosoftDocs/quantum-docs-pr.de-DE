---
uid: Microsoft.Quantum.Canon.RestrictedToSubregister
title: Restricteddesubregister-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: RestrictedToSubregister
qsharp.summary: Restricts an operation to an array of indices of a register, i.e., a subregister.
ms.openlocfilehash: a8b599035de6fede10bdaf8cef17f2124a59f064
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703854"
---
# <a name="restrictedtosubregister-function"></a><span data-ttu-id="fbec2-102">Restricteddesubregister-Funktion</span><span class="sxs-lookup"><span data-stu-id="fbec2-102">RestrictedToSubregister function</span></span>

<span data-ttu-id="fbec2-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="fbec2-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="fbec2-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="fbec2-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="fbec2-105">Schränkt einen Vorgang auf ein Array von Indizes eines Registers ein, d. h. ein unter Register.</span><span class="sxs-lookup"><span data-stu-id="fbec2-105">Restricts an operation to an array of indices of a register, i.e., a subregister.</span></span>

```qsharp
function RestrictedToSubregister (op : (Qubit[] => Unit), idxs : Int[]) : (Qubit[] => Unit)
```


## <a name="input"></a><span data-ttu-id="fbec2-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="fbec2-106">Input</span></span>

### <a name="op--qubit--unit"></a><span data-ttu-id="fbec2-107">OP: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="fbec2-107">op : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="fbec2-108">Der Vorgang, der auf ein unter Register beschränkt werden soll.</span><span class="sxs-lookup"><span data-stu-id="fbec2-108">Operation to be restricted to a subregister.</span></span>


### <a name="idxs--int"></a><span data-ttu-id="fbec2-109">idxs: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="fbec2-109">idxs : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="fbec2-110">Ein Array von Indizes, das angibt, auf welche Qubits der Vorgang beschränkt wird.</span><span class="sxs-lookup"><span data-stu-id="fbec2-110">Array of indices, indicating to which qubits the operation will be restricted.</span></span>



## <a name="output--qubit--unit"></a><span data-ttu-id="fbec2-111">Ausgabe: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="fbec2-111">Output : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 



## <a name="see-also"></a><span data-ttu-id="fbec2-112">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="fbec2-112">See Also</span></span>

- [<span data-ttu-id="fbec2-113">Microsoft. Quantum. Canon. restricteddesubregistera</span><span class="sxs-lookup"><span data-stu-id="fbec2-113">Microsoft.Quantum.Canon.RestrictedToSubregisterA</span></span>](xref:Microsoft.Quantum.Canon.RestrictedToSubregisterA)
- [<span data-ttu-id="fbec2-114">Microsoft. Quantum. Canon. restrictedto subregisterc</span><span class="sxs-lookup"><span data-stu-id="fbec2-114">Microsoft.Quantum.Canon.RestrictedToSubregisterC</span></span>](xref:Microsoft.Quantum.Canon.RestrictedToSubregisterC)
- [<span data-ttu-id="fbec2-115">Microsoft. Quantum. Canon. restrictedto subregisterca</span><span class="sxs-lookup"><span data-stu-id="fbec2-115">Microsoft.Quantum.Canon.RestrictedToSubregisterCA</span></span>](xref:Microsoft.Quantum.Canon.RestrictedToSubregisterCA)