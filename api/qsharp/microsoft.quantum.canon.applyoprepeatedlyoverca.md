---
uid: Microsoft.Quantum.Canon.ApplyOpRepeatedlyOverCA
title: Applyoprepeatedlyoverca-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyOpRepeatedlyOverCA
qsharp.summary: Applies the same op over a qubit register multiple times.
ms.openlocfilehash: b7d401f323d7affc27697744bb659c687e252682
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96209107"
---
# <a name="applyoprepeatedlyoverca-operation"></a><span data-ttu-id="31f68-102">Applyoprepeatedlyoverca-Vorgang</span><span class="sxs-lookup"><span data-stu-id="31f68-102">ApplyOpRepeatedlyOverCA operation</span></span>

<span data-ttu-id="31f68-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="31f68-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="31f68-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="31f68-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="31f68-105">Wendet denselben op-Vorgang über ein Qubit-Register mehrmals an.</span><span class="sxs-lookup"><span data-stu-id="31f68-105">Applies the same op over a qubit register multiple times.</span></span>

```qsharp
operation ApplyOpRepeatedlyOverCA (op : (Qubit[] => Unit is Adj + Ctl), targets : Int[][], register : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="31f68-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="31f68-106">Input</span></span>

### <a name="op--qubit--unit--is-adj--ctl"></a><span data-ttu-id="31f68-107">OP: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="31f68-107">op : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="31f68-108">Ein Vorgang, der mehrmals auf das Qubit-Register angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="31f68-108">An operation to be applied multiple times on the qubit register</span></span>


### <a name="targets--int"></a><span data-ttu-id="31f68-109">Ziele: [int](xref:microsoft.quantum.lang-ref.int)[] []</span><span class="sxs-lookup"><span data-stu-id="31f68-109">targets : [Int](xref:microsoft.quantum.lang-ref.int)[][]</span></span>

<span data-ttu-id="31f68-110">Geschmestete Arrays, die die Ziele des OP beschreiben.</span><span class="sxs-lookup"><span data-stu-id="31f68-110">Nested arrays describing the targets of the op.</span></span> <span data-ttu-id="31f68-111">Jedes Array muss eine Liste von int enthalten, die die zu verwendenden Qubits beschreibt.</span><span class="sxs-lookup"><span data-stu-id="31f68-111">Each array should contain a list of ints describing the qubits to be used.</span></span>


### <a name="register--qubit"></a><span data-ttu-id="31f68-112">Register: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="31f68-112">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="31f68-113">Das Qubit-Register, das bearbeitet werden soll.</span><span class="sxs-lookup"><span data-stu-id="31f68-113">Qubit register to be acted upon.</span></span>



## <a name="output--unit"></a><span data-ttu-id="31f68-114">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="31f68-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="31f68-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="31f68-115">See Also</span></span>

- [<span data-ttu-id="31f68-116">Microsoft. Quantum. Canon. applyseriesofops</span><span class="sxs-lookup"><span data-stu-id="31f68-116">Microsoft.Quantum.Canon.ApplySeriesOfOps</span></span>](xref:Microsoft.Quantum.Canon.ApplySeriesOfOps)