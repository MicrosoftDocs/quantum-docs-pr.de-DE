---
uid: Microsoft.Quantum.Diagnostics.AssertOperationsEqualInPlace
title: Assertoperationsequalinplace-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertOperationsEqualInPlace
qsharp.summary: >-
  Given two operations, asserts that they act identically for all input states.

  This assertion is implemented by checking the action of the operations on all states of the form $V_0 \otimes ... \otimes V_{n-1}$, where $V_k$ is one of the states $\ket{0}$, $\ket{1}$, $\ket{+}$ and $\ket{i}$ (+1 eigenstate of Pauli Y operator).

  This assertion uses $n$ qubits and requires multiple calls of the operations being compared.
ms.openlocfilehash: 407a139da816281346eb06849f81e91b83202653
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702755"
---
# <a name="assertoperationsequalinplace-operation"></a><span data-ttu-id="ed82a-102">Assertoperationsequalinplace-Vorgang</span><span class="sxs-lookup"><span data-stu-id="ed82a-102">AssertOperationsEqualInPlace operation</span></span>

<span data-ttu-id="ed82a-103">Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="ed82a-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="ed82a-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="ed82a-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="ed82a-105">Bei zwei Vorgängen wird von bestätigt, dass Sie für alle Eingabe Zustände identisch agieren.</span><span class="sxs-lookup"><span data-stu-id="ed82a-105">Given two operations, asserts that they act identically for all input states.</span></span>

<span data-ttu-id="ed82a-106">Diese Assertionen werden implementiert, indem die Aktion der Vorgänge für alle Zustände der Form $V _0 \otimes... \otimes v_ {n-1} $, wobei $V _K $ einem der Zustände $ \ket {0} $, $ \ket {1} $, $ \ket{+} $ und $ \ket{i} $ (+ 1 eigen Status des Pauli Y-Operators) entspricht.</span><span class="sxs-lookup"><span data-stu-id="ed82a-106">This assertion is implemented by checking the action of the operations on all states of the form $V_0 \otimes ... \otimes V_{n-1}$, where $V_k$ is one of the states $\ket{0}$, $\ket{1}$, $\ket{+}$ and $\ket{i}$ (+1 eigenstate of Pauli Y operator).</span></span>

<span data-ttu-id="ed82a-107">Diese Assertion verwendet $n $ Qubits und erfordert mehrere Aufrufe der zu vergleichenden Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="ed82a-107">This assertion uses $n$ qubits and requires multiple calls of the operations being compared.</span></span>

```qsharp
operation AssertOperationsEqualInPlace (nQubits : Int, givenU : (Qubit[] => Unit), expectedU : (Qubit[] => Unit is Adj)) : Unit
```


## <a name="input"></a><span data-ttu-id="ed82a-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ed82a-108">Input</span></span>

### <a name="nqubits--int"></a><span data-ttu-id="ed82a-109">nqubits: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="ed82a-109">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="ed82a-110">Die Anzahl der Qubits $n $, an denen die Vorgänge ausgeführt werden `givenU` `expectedU` .</span><span class="sxs-lookup"><span data-stu-id="ed82a-110">The number of qubits $n$ that the operations `givenU` and `expectedU` operate on.</span></span>


### <a name="givenu--qubit--unit"></a><span data-ttu-id="ed82a-111">givenu: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="ed82a-111">givenU : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="ed82a-112">Der Vorgang auf $n $ Qubits, der geprüft werden soll.</span><span class="sxs-lookup"><span data-stu-id="ed82a-112">Operation on $n$ qubits to be checked.</span></span>


### <a name="expectedu--qubit--unit-adj"></a><span data-ttu-id="ed82a-113">expectedu: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ</span><span class="sxs-lookup"><span data-stu-id="ed82a-113">expectedU : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="ed82a-114">Verweis Vorgang auf $n $ Qubits, der mit `givenU` verglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="ed82a-114">Reference operation on $n$ qubits that `givenU` is to be compared against.</span></span>



## <a name="output--unit"></a><span data-ttu-id="ed82a-115">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="ed82a-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="references"></a><span data-ttu-id="ed82a-116">Referenzen</span><span class="sxs-lookup"><span data-stu-id="ed82a-116">References</span></span>

<span data-ttu-id="ed82a-117">Die Basis der Zustände $ \ket {0} $, $ \ket {1} $, $ \ket{+} $ und $ \ket{i} $ ist die Chuang-Nielsen Basis, die unter [ *i. L. Chuang, M. A. Nielsen*](https://arxiv.org/abs/quant-ph/9610001)beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="ed82a-117">The basis of states $\ket{0}$, $\ket{1}$, $\ket{+}$ and $\ket{i}$ is the Chuang-Nielsen basis, described in [ *I. L. Chuang, M. A. Nielsen* ](https://arxiv.org/abs/quant-ph/9610001).</span></span>

## <a name="see-also"></a><span data-ttu-id="ed82a-118">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ed82a-118">See Also</span></span>

- [<span data-ttu-id="ed82a-119">Microsoft. Quantum. Diagnostics. assertoperationsequalreferenziert</span><span class="sxs-lookup"><span data-stu-id="ed82a-119">Microsoft.Quantum.Diagnostics.AssertOperationsEqualReferenced</span></span>](xref:Microsoft.Quantum.Diagnostics.AssertOperationsEqualReferenced)