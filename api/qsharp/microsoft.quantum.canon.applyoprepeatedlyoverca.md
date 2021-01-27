---
uid: Microsoft.Quantum.Canon.ApplyOpRepeatedlyOverCA
title: Applyoprepeatedlyoverca-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyOpRepeatedlyOverCA
qsharp.summary: Applies the same op over a qubit register multiple times.
ms.openlocfilehash: 9b7f0897009d9913fc886f99b2e29f3fc1040666
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841604"
---
# <a name="applyoprepeatedlyoverca-operation"></a><span data-ttu-id="dad34-102">Applyoprepeatedlyoverca-Vorgang</span><span class="sxs-lookup"><span data-stu-id="dad34-102">ApplyOpRepeatedlyOverCA operation</span></span>

<span data-ttu-id="dad34-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="dad34-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="dad34-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="dad34-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="dad34-105">Wendet denselben op-Vorgang über ein Qubit-Register mehrmals an.</span><span class="sxs-lookup"><span data-stu-id="dad34-105">Applies the same op over a qubit register multiple times.</span></span>

```qsharp
operation ApplyOpRepeatedlyOverCA (op : (Qubit[] => Unit is Adj + Ctl), targets : Int[][], register : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="dad34-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="dad34-106">Input</span></span>

### <a name="op--qubit--unit--is-adj--ctl"></a><span data-ttu-id="dad34-107">OP: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="dad34-107">op : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="dad34-108">Ein Vorgang, der mehrmals auf das Qubit-Register angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="dad34-108">An operation to be applied multiple times on the qubit register</span></span>


### <a name="targets--int"></a><span data-ttu-id="dad34-109">Ziele: [int](xref:microsoft.quantum.lang-ref.int)[] []</span><span class="sxs-lookup"><span data-stu-id="dad34-109">targets : [Int](xref:microsoft.quantum.lang-ref.int)[][]</span></span>

<span data-ttu-id="dad34-110">Geschmestete Arrays, die die Ziele des OP beschreiben.</span><span class="sxs-lookup"><span data-stu-id="dad34-110">Nested arrays describing the targets of the op.</span></span> <span data-ttu-id="dad34-111">Jedes Array muss eine Liste von int enthalten, die die zu verwendenden Qubits beschreibt.</span><span class="sxs-lookup"><span data-stu-id="dad34-111">Each array should contain a list of ints describing the qubits to be used.</span></span>


### <a name="register--qubit"></a><span data-ttu-id="dad34-112">Register: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="dad34-112">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="dad34-113">Das Qubit-Register, das bearbeitet werden soll.</span><span class="sxs-lookup"><span data-stu-id="dad34-113">Qubit register to be acted upon.</span></span>



## <a name="output--unit"></a><span data-ttu-id="dad34-114">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="dad34-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="dad34-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="dad34-115">See Also</span></span>

- [<span data-ttu-id="dad34-116">Microsoft. Quantum. Canon. applyseriesofops</span><span class="sxs-lookup"><span data-stu-id="dad34-116">Microsoft.Quantum.Canon.ApplySeriesOfOps</span></span>](xref:Microsoft.Quantum.Canon.ApplySeriesOfOps)