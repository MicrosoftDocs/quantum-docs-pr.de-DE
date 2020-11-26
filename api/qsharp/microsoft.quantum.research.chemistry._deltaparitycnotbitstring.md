---
uid: Microsoft.Quantum.Research.Chemistry._DeltaParityCNOTbitstring
title: _DeltaParityCNOTbitstring-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Research.Chemistry
qsharp.name: _DeltaParityCNOTbitstring
qsharp.summary: Classical processing step of `ApplyDeltaParity`. This computes a list of control qubits for evaluating parity difference between any two PQRS... terms of even length.
ms.openlocfilehash: 0c0da60e3c389f8208f9f7d5c84a09893f3c1bda
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96226076"
---
# <a name="_deltaparitycnotbitstring-function"></a><span data-ttu-id="6f942-102">_DeltaParityCNOTbitstring-Funktion</span><span class="sxs-lookup"><span data-stu-id="6f942-102">_DeltaParityCNOTbitstring function</span></span>

<span data-ttu-id="6f942-103">Namespace: [Microsoft. Quantum. Research. Chemistry](xref:Microsoft.Quantum.Research.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="6f942-103">Namespace: [Microsoft.Quantum.Research.Chemistry](xref:Microsoft.Quantum.Research.Chemistry)</span></span>

<span data-ttu-id="6f942-104">Paket: [Microsoft. Quantum. Research. Chemistry](https://nuget.org/packages/Microsoft.Quantum.Research.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="6f942-104">Package: [Microsoft.Quantum.Research.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Research.Chemistry)</span></span>


<span data-ttu-id="6f942-105">Klassischer Verarbeitungsschritt von `ApplyDeltaParity` .</span><span class="sxs-lookup"><span data-stu-id="6f942-105">Classical processing step of `ApplyDeltaParity`.</span></span>
<span data-ttu-id="6f942-106">Dadurch wird eine Liste von Steuerungs-Qubits zum Auswerten der Paritäts Unterschiede zwischen zwei pqrs berechnet... Begriffe der geraden Länge.</span><span class="sxs-lookup"><span data-stu-id="6f942-106">This computes a list of control qubits for evaluating parity difference between any two PQRS... terms of even length.</span></span>

```qsharp
function _DeltaParityCNOTbitstring (prevFermionicTerm : Int[], nextFermionicTerm : Int[]) : (Int, Bool[])
```


## <a name="input"></a><span data-ttu-id="6f942-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6f942-107">Input</span></span>

### <a name="prevfermionicterm--int"></a><span data-ttu-id="6f942-108">prevfermionicterm: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="6f942-108">prevFermionicTerm : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>




### <a name="nextfermionicterm--int"></a><span data-ttu-id="6f942-109">nextfermionicterm: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="6f942-109">nextFermionicTerm : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>





## <a name="output--intbool"></a><span data-ttu-id="6f942-110">Ausgabe: ([int](xref:microsoft.quantum.lang-ref.int),[bool](xref:microsoft.quantum.lang-ref.bool)[])</span><span class="sxs-lookup"><span data-stu-id="6f942-110">Output : ([Int](xref:microsoft.quantum.lang-ref.int),[Bool](xref:microsoft.quantum.lang-ref.bool)[])</span></span>



## <a name="remarks"></a><span data-ttu-id="6f942-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6f942-111">Remarks</span></span>

<span data-ttu-id="6f942-112">Dabei wird davon ausgegangen, dass die Länge der Begriffe gleich ist.</span><span class="sxs-lookup"><span data-stu-id="6f942-112">This assumes that the length of terms is even.</span></span>
<span data-ttu-id="6f942-113">Berechnet die Liste der Steuerelemente für den Paritäts Unterschied zwischen zwei Begriffen.</span><span class="sxs-lookup"><span data-stu-id="6f942-113">Computes list of controls for parity difference between any two terms.</span></span>
<span data-ttu-id="6f942-114">Dabei wird davon ausgegangen, dass die Eingabe Listen in aufsteigender Reihenfolge sortiert sind.</span><span class="sxs-lookup"><span data-stu-id="6f942-114">This assumes that the input lists is sorted in ascending order.</span></span>