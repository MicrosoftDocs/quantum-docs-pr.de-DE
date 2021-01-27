---
uid: Microsoft.Quantum.Diagnostics.AssertOperationsEqualInPlaceCompBasis
title: Assertoperationsequalinplacecompbasis-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertOperationsEqualInPlaceCompBasis
qsharp.summary: Checks if the operation `givenU` is equal to the operation `expectedU` on the given input size  by checking the action of the operations only on the vectors from the computational basis. This is a necessary, but not sufficient, condition for the equality of two unitaries.
ms.openlocfilehash: f9d3aaf7e774cf2495ca69382db2470d1d0fa7b5
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98830481"
---
# <a name="assertoperationsequalinplacecompbasis-operation"></a><span data-ttu-id="9a4d0-102">Assertoperationsequalinplacecompbasis-Vorgang</span><span class="sxs-lookup"><span data-stu-id="9a4d0-102">AssertOperationsEqualInPlaceCompBasis operation</span></span>

<span data-ttu-id="9a4d0-103">Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="9a4d0-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="9a4d0-104">Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="9a4d0-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="9a4d0-105">Überprüft, ob der Vorgang mit `givenU` dem Vorgang `expectedU` auf der angegebenen Eingabe Größe identisch ist, indem die Aktion der Vorgänge nur für die Vektoren von der Berechnungsbasis überprüft wird.</span><span class="sxs-lookup"><span data-stu-id="9a4d0-105">Checks if the operation `givenU` is equal to the operation `expectedU` on the given input size  by checking the action of the operations only on the vectors from the computational basis.</span></span>
<span data-ttu-id="9a4d0-106">Dies ist eine erforderliche, aber nicht ausreichende Bedingung für die Gleichheit von zwei uniflüssen.</span><span class="sxs-lookup"><span data-stu-id="9a4d0-106">This is a necessary, but not sufficient, condition for the equality of two unitaries.</span></span>

```qsharp
operation AssertOperationsEqualInPlaceCompBasis (nQubits : Int, givenU : (Qubit[] => Unit), expectedU : (Qubit[] => Unit is Adj)) : Unit
```


## <a name="input"></a><span data-ttu-id="9a4d0-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="9a4d0-107">Input</span></span>

### <a name="nqubits--int"></a><span data-ttu-id="9a4d0-108">nqubits: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="9a4d0-108">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="9a4d0-109">Die Anzahl der Qubits $n $, an denen die Vorgänge ausgeführt werden `givenU` `expectedU` .</span><span class="sxs-lookup"><span data-stu-id="9a4d0-109">The number of qubits $n$ that the operations `givenU` and `expectedU` operate on.</span></span>


### <a name="givenu--qubit--unit"></a><span data-ttu-id="9a4d0-110">givenu: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="9a4d0-110">givenU : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="9a4d0-111">Der Vorgang auf $n $ Qubits, der geprüft werden soll.</span><span class="sxs-lookup"><span data-stu-id="9a4d0-111">Operation on $n$ qubits to be checked.</span></span>


### <a name="expectedu--qubit--unit--is-adj"></a><span data-ttu-id="9a4d0-112">expectedu: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ</span><span class="sxs-lookup"><span data-stu-id="9a4d0-112">expectedU : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="9a4d0-113">Verweis Vorgang auf $n $ Qubits, der mit `givenU` verglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="9a4d0-113">Reference operation on $n$ qubits that `givenU` is to be compared against.</span></span>



## <a name="output--unit"></a><span data-ttu-id="9a4d0-114">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="9a4d0-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

