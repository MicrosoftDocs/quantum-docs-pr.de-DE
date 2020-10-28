---
uid: Microsoft.Quantum.Canon.ApplyOpRepeatedlyOver
title: Applyoprepeatedlyover-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyOpRepeatedlyOver
qsharp.summary: Applies the same op over a qubit register multiple times.
ms.openlocfilehash: 09f54be33a7b5c58a317a949290f5cd6d54fe841
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705130"
---
# <a name="applyoprepeatedlyover-operation"></a><span data-ttu-id="4c0f0-102">Applyoprepeatedlyover-Vorgang</span><span class="sxs-lookup"><span data-stu-id="4c0f0-102">ApplyOpRepeatedlyOver operation</span></span>

<span data-ttu-id="4c0f0-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="4c0f0-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="4c0f0-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="4c0f0-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="4c0f0-105">Wendet denselben op-Vorgang über ein Qubit-Register mehrmals an.</span><span class="sxs-lookup"><span data-stu-id="4c0f0-105">Applies the same op over a qubit register multiple times.</span></span>

```qsharp
operation ApplyOpRepeatedlyOver (op : (Qubit[] => Unit), targets : Int[][], register : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="4c0f0-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="4c0f0-106">Input</span></span>

### <a name="op--qubit--unit"></a><span data-ttu-id="4c0f0-107">OP: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="4c0f0-107">op : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="4c0f0-108">Ein Vorgang, der mehrmals auf das Qubit-Register angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="4c0f0-108">An operation to be applied multiple times on the qubit register</span></span>


### <a name="targets--int"></a><span data-ttu-id="4c0f0-109">Ziele: [int](xref:microsoft.quantum.lang-ref.int)[] []</span><span class="sxs-lookup"><span data-stu-id="4c0f0-109">targets : [Int](xref:microsoft.quantum.lang-ref.int)[][]</span></span>

<span data-ttu-id="4c0f0-110">Geschmestete Arrays, die die Ziele des OP beschreiben.</span><span class="sxs-lookup"><span data-stu-id="4c0f0-110">Nested arrays describing the targets of the op.</span></span> <span data-ttu-id="4c0f0-111">Jedes Array muss eine Liste von int enthalten, die die zu verwendenden Qubits beschreibt.</span><span class="sxs-lookup"><span data-stu-id="4c0f0-111">Each array should contain a list of ints describing the qubits to be used.</span></span>


### <a name="register--qubit"></a><span data-ttu-id="4c0f0-112">Register: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="4c0f0-112">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="4c0f0-113">Das Qubit-Register, das bearbeitet werden soll.</span><span class="sxs-lookup"><span data-stu-id="4c0f0-113">Qubit register to be acted upon.</span></span>



## <a name="output--unit"></a><span data-ttu-id="4c0f0-114">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="4c0f0-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="4c0f0-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="4c0f0-115">See Also</span></span>

- [<span data-ttu-id="4c0f0-116">Microsoft. Quantum. Canon. applyseriesofops</span><span class="sxs-lookup"><span data-stu-id="4c0f0-116">Microsoft.Quantum.Canon.ApplySeriesOfOps</span></span>](xref:Microsoft.Quantum.Canon.ApplySeriesOfOps)