---
uid: Microsoft.Quantum.Diagnostics.AssertOperationsEqualInPlaceCompBasis
title: Assertoperationsequalinplacecompbasis-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertOperationsEqualInPlaceCompBasis
qsharp.summary: Checks if the operation `givenU` is equal to the operation `expectedU` on the given input size  by checking the action of the operations only on the vectors from the computational basis. This is a necessary, but not sufficient, condition for the equality of two unitaries.
ms.openlocfilehash: 826369bdf3544fb257c2bb202466426c1ca1e113
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96202344"
---
# <a name="assertoperationsequalinplacecompbasis-operation"></a><span data-ttu-id="e42e2-102">Assertoperationsequalinplacecompbasis-Vorgang</span><span class="sxs-lookup"><span data-stu-id="e42e2-102">AssertOperationsEqualInPlaceCompBasis operation</span></span>

<span data-ttu-id="e42e2-103">Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="e42e2-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="e42e2-104">Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="e42e2-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="e42e2-105">Überprüft, ob der Vorgang mit `givenU` dem Vorgang `expectedU` auf der angegebenen Eingabe Größe identisch ist, indem die Aktion der Vorgänge nur für die Vektoren von der Berechnungsbasis überprüft wird.</span><span class="sxs-lookup"><span data-stu-id="e42e2-105">Checks if the operation `givenU` is equal to the operation `expectedU` on the given input size  by checking the action of the operations only on the vectors from the computational basis.</span></span>
<span data-ttu-id="e42e2-106">Dies ist eine erforderliche, aber nicht ausreichende Bedingung für die Gleichheit von zwei uniflüssen.</span><span class="sxs-lookup"><span data-stu-id="e42e2-106">This is a necessary, but not sufficient, condition for the equality of two unitaries.</span></span>

```qsharp
operation AssertOperationsEqualInPlaceCompBasis (nQubits : Int, givenU : (Qubit[] => Unit), expectedU : (Qubit[] => Unit is Adj)) : Unit
```


## <a name="input"></a><span data-ttu-id="e42e2-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e42e2-107">Input</span></span>

### <a name="nqubits--int"></a><span data-ttu-id="e42e2-108">nqubits: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="e42e2-108">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="e42e2-109">Die Anzahl der Qubits $n $, an denen die Vorgänge ausgeführt werden `givenU` `expectedU` .</span><span class="sxs-lookup"><span data-stu-id="e42e2-109">The number of qubits $n$ that the operations `givenU` and `expectedU` operate on.</span></span>


### <a name="givenu--qubit--unit"></a><span data-ttu-id="e42e2-110">givenu: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="e42e2-110">givenU : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="e42e2-111">Der Vorgang auf $n $ Qubits, der geprüft werden soll.</span><span class="sxs-lookup"><span data-stu-id="e42e2-111">Operation on $n$ qubits to be checked.</span></span>


### <a name="expectedu--qubit--unit--is-adj"></a><span data-ttu-id="e42e2-112">expectedu: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ</span><span class="sxs-lookup"><span data-stu-id="e42e2-112">expectedU : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="e42e2-113">Verweis Vorgang auf $n $ Qubits, der mit `givenU` verglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="e42e2-113">Reference operation on $n$ qubits that `givenU` is to be compared against.</span></span>



## <a name="output--unit"></a><span data-ttu-id="e42e2-114">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="e42e2-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

