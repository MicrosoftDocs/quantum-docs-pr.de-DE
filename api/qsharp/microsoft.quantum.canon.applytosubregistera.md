---
uid: Microsoft.Quantum.Canon.ApplyToSubregisterA
title: Applydesubregistera-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToSubregisterA
qsharp.summary: Applies an operation to a subregister of a register, with qubits specified by an array of their indices. The modifier `A` indicates that the operation is adjointable.
ms.openlocfilehash: 7a5ae78edcda363f21cadaaed5cb273d35cb60cc
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841228"
---
# <a name="applytosubregistera-operation"></a><span data-ttu-id="f35af-102">Applydesubregistera-Vorgang</span><span class="sxs-lookup"><span data-stu-id="f35af-102">ApplyToSubregisterA operation</span></span>

<span data-ttu-id="f35af-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="f35af-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="f35af-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="f35af-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="f35af-105">Wendet einen Vorgang auf ein unter Register eines Register mit Qubits an, die durch ein Array ihrer Indizes angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="f35af-105">Applies an operation to a subregister of a register, with qubits specified by an array of their indices.</span></span>
<span data-ttu-id="f35af-106">Der-Modifizierer `A` gibt an, dass der Vorgang adjointable ist.</span><span class="sxs-lookup"><span data-stu-id="f35af-106">The modifier `A` indicates that the operation is adjointable.</span></span>

```qsharp
operation ApplyToSubregisterA (op : (Qubit[] => Unit is Adj), idxs : Int[], target : Qubit[]) : Unit is Adj
```


## <a name="input"></a><span data-ttu-id="f35af-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f35af-107">Input</span></span>

### <a name="op--qubit--unit--is-adj"></a><span data-ttu-id="f35af-108">OP: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ</span><span class="sxs-lookup"><span data-stu-id="f35af-108">op : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="f35af-109">Der für die unter Registrierung anzuwendende Vorgang.</span><span class="sxs-lookup"><span data-stu-id="f35af-109">Operation to apply to subregister.</span></span>


### <a name="idxs--int"></a><span data-ttu-id="f35af-110">idxs: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="f35af-110">idxs : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="f35af-111">Ein Array von Indizes, das angibt, auf welche Qubits der Vorgang angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="f35af-111">Array of indices, indicating to which qubits the operation will be applied.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="f35af-112">Ziel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="f35af-112">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="f35af-113">Registrieren Sie sich für den Vorgang.</span><span class="sxs-lookup"><span data-stu-id="f35af-113">Register on which the operation acts.</span></span>



## <a name="output--unit"></a><span data-ttu-id="f35af-114">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="f35af-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="f35af-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="f35af-115">See Also</span></span>

- [<span data-ttu-id="f35af-116">Microsoft. Quantum. Canon. applydesubregister</span><span class="sxs-lookup"><span data-stu-id="f35af-116">Microsoft.Quantum.Canon.ApplyToSubregister</span></span>](xref:Microsoft.Quantum.Canon.ApplyToSubregister)