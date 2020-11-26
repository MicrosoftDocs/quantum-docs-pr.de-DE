---
uid: Microsoft.Quantum.Diagnostics.AssertOperationsEqualReferenced
title: Assertoperationsequalreferenzierter Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertOperationsEqualReferenced
qsharp.summary: >-
  Given two operations, asserts that they act identically for all input states.

  This assertion is implemented by using the Choi–Jamiołkowski isomorphism to reduce the assertion to one of a qubit state assertion on two entangled registers. Thus, this operation needs only a single call to each operation being tested, but requires twice as many qubits to be allocated. This assertion can be used to ensure, for instance, that an optimized version of an operation acts identically to its naïve implementation, or that an operation which acts on a range of non-quantum inputs agrees with known cases.
ms.openlocfilehash: 59c0fa72c9ca8f3bc512b6ed674fd73babc57f84
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96202310"
---
# <a name="assertoperationsequalreferenced-operation"></a><span data-ttu-id="337e5-102">Assertoperationsequalreferenzierter Vorgang</span><span class="sxs-lookup"><span data-stu-id="337e5-102">AssertOperationsEqualReferenced operation</span></span>

<span data-ttu-id="337e5-103">Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="337e5-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="337e5-104">Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="337e5-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="337e5-105">Bei zwei Vorgängen wird von bestätigt, dass Sie für alle Eingabe Zustände identisch agieren.</span><span class="sxs-lookup"><span data-stu-id="337e5-105">Given two operations, asserts that they act identically for all input states.</span></span>

<span data-ttu-id="337e5-106">Diese Assertionen werden mithilfe von "Choi – jamiołkowski" (isomorphism) implementiert, um die Behauptung auf eine der Qubit-Zustands Assertionen für zwei entkoppelt-Register zu reduzieren.</span><span class="sxs-lookup"><span data-stu-id="337e5-106">This assertion is implemented by using the Choi–Jamiołkowski isomorphism to reduce the assertion to one of a qubit state assertion on two entangled registers.</span></span>
<span data-ttu-id="337e5-107">Folglich benötigt dieser Vorgang nur einen einzelnen Vorgang für jeden zu testenden Vorgang, erfordert jedoch doppelt so viele Qubits, die zugewiesen werden müssen.</span><span class="sxs-lookup"><span data-stu-id="337e5-107">Thus, this operation needs only a single call to each operation being tested, but requires twice as many qubits to be allocated.</span></span>
<span data-ttu-id="337e5-108">Diese Assertion kann beispielsweise verwendet werden, um sicherzustellen, dass eine optimierte Version eines Vorgangs identisch mit der naive Implementierung verhält oder dass ein Vorgang, der für einen Bereich von nicht-Quantum-Eingaben agiert, mit bekannten Fällen übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="337e5-108">This assertion can be used to ensure, for instance, that an optimized version of an operation acts identically to its naïve implementation, or that an operation which acts on a range of non-quantum inputs agrees with known cases.</span></span>

```qsharp
operation AssertOperationsEqualReferenced (nQubits : Int, actual : (Qubit[] => Unit), expected : (Qubit[] => Unit is Adj)) : Unit
```


## <a name="input"></a><span data-ttu-id="337e5-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="337e5-109">Input</span></span>

### <a name="nqubits--int"></a><span data-ttu-id="337e5-110">nqubits: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="337e5-110">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="337e5-111">Anzahl von Qubits, die an jeden Vorgang übergeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="337e5-111">Number of qubits to pass to each operation.</span></span>


### <a name="actual--qubit--unit"></a><span data-ttu-id="337e5-112">tatsächlicher Wert: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="337e5-112">actual : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="337e5-113">Zu testender Vorgang.</span><span class="sxs-lookup"><span data-stu-id="337e5-113">Operation to be tested.</span></span>


### <a name="expected--qubit--unit--is-adj"></a><span data-ttu-id="337e5-114">erwartet: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ</span><span class="sxs-lookup"><span data-stu-id="337e5-114">expected : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="337e5-115">Vorgang, der das erwartete Verhalten für den zu testenden Vorgang definiert.</span><span class="sxs-lookup"><span data-stu-id="337e5-115">Operation defining the expected behavior for the operation under test.</span></span>



## <a name="output--unit"></a><span data-ttu-id="337e5-116">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="337e5-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="337e5-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="337e5-117">Remarks</span></span>

<span data-ttu-id="337e5-118">Dieser Vorgang erfordert, dass der Vorgang, der das erwartete Verhalten modelliert, adjointable ist, sodass die Umkehrung nur für das Ziel Register ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="337e5-118">This operation requires that the operation modeling the expected behavior is adjointable, so that the inverse can be performed on the target register alone.</span></span>
<span data-ttu-id="337e5-119">Formal kann ein Vorgang zum Austauschen angegeben werden, der diese Anforderung lockert, aber der Vorgang zum Austauschen ist nicht im allgemeinen physisch für beliebige Quantum-Vorgänge physisch realisierbar und daher hier nicht als Option enthalten.</span><span class="sxs-lookup"><span data-stu-id="337e5-119">Formally, one can specify a transpose operation, which relaxes this requirement, but the transpose operation is not in general physically realizable for arbitrary quantum operations and thus is not included here as an option.</span></span>