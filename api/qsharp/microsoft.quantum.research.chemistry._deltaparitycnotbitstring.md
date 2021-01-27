---
uid: Microsoft.Quantum.Research.Chemistry._DeltaParityCNOTbitstring
title: _DeltaParityCNOTbitstring-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Research.Chemistry
qsharp.name: _DeltaParityCNOTbitstring
qsharp.summary: Classical processing step of `ApplyDeltaParity`. This computes a list of control qubits for evaluating parity difference between any two PQRS... terms of even length.
ms.openlocfilehash: 3dd2d299a094577d377780d731e76287815e8d03
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98847601"
---
# <a name="_deltaparitycnotbitstring-function"></a><span data-ttu-id="ec2fe-102">_DeltaParityCNOTbitstring-Funktion</span><span class="sxs-lookup"><span data-stu-id="ec2fe-102">_DeltaParityCNOTbitstring function</span></span>

<span data-ttu-id="ec2fe-103">Namespace: [Microsoft. Quantum. Research. Chemistry](xref:Microsoft.Quantum.Research.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="ec2fe-103">Namespace: [Microsoft.Quantum.Research.Chemistry](xref:Microsoft.Quantum.Research.Chemistry)</span></span>

<span data-ttu-id="ec2fe-104">Paket: [Microsoft. Quantum. Research. Chemistry](https://nuget.org/packages/Microsoft.Quantum.Research.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="ec2fe-104">Package: [Microsoft.Quantum.Research.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Research.Chemistry)</span></span>


<span data-ttu-id="ec2fe-105">Klassischer Verarbeitungsschritt von `ApplyDeltaParity` .</span><span class="sxs-lookup"><span data-stu-id="ec2fe-105">Classical processing step of `ApplyDeltaParity`.</span></span>
<span data-ttu-id="ec2fe-106">Dadurch wird eine Liste von Steuerungs-Qubits zum Auswerten der Paritäts Unterschiede zwischen zwei pqrs berechnet... Begriffe der geraden Länge.</span><span class="sxs-lookup"><span data-stu-id="ec2fe-106">This computes a list of control qubits for evaluating parity difference between any two PQRS... terms of even length.</span></span>

```qsharp
function _DeltaParityCNOTbitstring (prevFermionicTerm : Int[], nextFermionicTerm : Int[]) : (Int, Bool[])
```


## <a name="input"></a><span data-ttu-id="ec2fe-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ec2fe-107">Input</span></span>

### <a name="prevfermionicterm--int"></a><span data-ttu-id="ec2fe-108">prevfermionicterm: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="ec2fe-108">prevFermionicTerm : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>




### <a name="nextfermionicterm--int"></a><span data-ttu-id="ec2fe-109">nextfermionicterm: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="ec2fe-109">nextFermionicTerm : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>





## <a name="output--intbool"></a><span data-ttu-id="ec2fe-110">Ausgabe: ([int](xref:microsoft.quantum.lang-ref.int),[bool](xref:microsoft.quantum.lang-ref.bool)[])</span><span class="sxs-lookup"><span data-stu-id="ec2fe-110">Output : ([Int](xref:microsoft.quantum.lang-ref.int),[Bool](xref:microsoft.quantum.lang-ref.bool)[])</span></span>



## <a name="remarks"></a><span data-ttu-id="ec2fe-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ec2fe-111">Remarks</span></span>

<span data-ttu-id="ec2fe-112">Dabei wird davon ausgegangen, dass die Länge der Begriffe gleich ist.</span><span class="sxs-lookup"><span data-stu-id="ec2fe-112">This assumes that the length of terms is even.</span></span>
<span data-ttu-id="ec2fe-113">Berechnet die Liste der Steuerelemente für den Paritäts Unterschied zwischen zwei Begriffen.</span><span class="sxs-lookup"><span data-stu-id="ec2fe-113">Computes list of controls for parity difference between any two terms.</span></span>
<span data-ttu-id="ec2fe-114">Dabei wird davon ausgegangen, dass die Eingabe Listen in aufsteigender Reihenfolge sortiert sind.</span><span class="sxs-lookup"><span data-stu-id="ec2fe-114">This assumes that the input lists is sorted in ascending order.</span></span>