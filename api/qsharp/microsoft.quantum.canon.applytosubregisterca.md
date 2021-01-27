---
uid: Microsoft.Quantum.Canon.ApplyToSubregisterCA
title: Applydesubregisterca-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToSubregisterCA
qsharp.summary: Applies an operation to a subregister of a register, with qubits specified by an array of their indices. The modifier `CA` indicates that the operation is controllable and adjointable.
ms.openlocfilehash: 9f24c3ca9b152cf9bbf81e59b86f83a0ab459031
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841207"
---
# <a name="applytosubregisterca-operation"></a><span data-ttu-id="884f0-102">Applydesubregisterca-Vorgang</span><span class="sxs-lookup"><span data-stu-id="884f0-102">ApplyToSubregisterCA operation</span></span>

<span data-ttu-id="884f0-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="884f0-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="884f0-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="884f0-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="884f0-105">Wendet einen Vorgang auf ein unter Register eines Register mit Qubits an, die durch ein Array ihrer Indizes angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="884f0-105">Applies an operation to a subregister of a register, with qubits specified by an array of their indices.</span></span>
<span data-ttu-id="884f0-106">Der-Modifizierer `CA` gibt an, dass der Vorgang steuerbar und adjointable ist.</span><span class="sxs-lookup"><span data-stu-id="884f0-106">The modifier `CA` indicates that the operation is controllable and adjointable.</span></span>

```qsharp
operation ApplyToSubregisterCA (op : (Qubit[] => Unit is Ctl + Adj), idxs : Int[], target : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="884f0-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="884f0-107">Input</span></span>

### <a name="op--qubit--unit--is-adj--ctl"></a><span data-ttu-id="884f0-108">OP: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="884f0-108">op : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="884f0-109">Der für die unter Registrierung anzuwendende Vorgang.</span><span class="sxs-lookup"><span data-stu-id="884f0-109">Operation to apply to subregister.</span></span>


### <a name="idxs--int"></a><span data-ttu-id="884f0-110">idxs: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="884f0-110">idxs : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="884f0-111">Ein Array von Indizes, das angibt, auf welche Qubits der Vorgang angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="884f0-111">Array of indices, indicating to which qubits the operation will be applied.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="884f0-112">Ziel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="884f0-112">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="884f0-113">Registrieren Sie sich für den Vorgang.</span><span class="sxs-lookup"><span data-stu-id="884f0-113">Register on which the operation acts.</span></span>



## <a name="output--unit"></a><span data-ttu-id="884f0-114">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="884f0-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="884f0-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="884f0-115">See Also</span></span>

- [<span data-ttu-id="884f0-116">Microsoft. Quantum. Canon. applydesubregister</span><span class="sxs-lookup"><span data-stu-id="884f0-116">Microsoft.Quantum.Canon.ApplyToSubregister</span></span>](xref:Microsoft.Quantum.Canon.ApplyToSubregister)