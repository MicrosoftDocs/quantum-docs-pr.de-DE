---
uid: Microsoft.Quantum.Research.Chemistry._DeltaParityCNOTbitstring
title: _DeltaParityCNOTbitstring-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Research.Chemistry
qsharp.name: _DeltaParityCNOTbitstring
qsharp.summary: Classical processing step of `ApplyDeltaParity`. This computes a list of control qubits for evaluating parity difference between any two PQRS... terms of even length.
ms.openlocfilehash: 95b4c2df05f32cb937ec2cf421f43f2fdbf319da
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92701844"
---
# <a name="_deltaparitycnotbitstring-function"></a><span data-ttu-id="f8cab-102">_DeltaParityCNOTbitstring-Funktion</span><span class="sxs-lookup"><span data-stu-id="f8cab-102">_DeltaParityCNOTbitstring function</span></span>

<span data-ttu-id="f8cab-103">Namespace: [Microsoft. Quantum. Research. Chemistry](xref:Microsoft.Quantum.Research.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="f8cab-103">Namespace: [Microsoft.Quantum.Research.Chemistry](xref:Microsoft.Quantum.Research.Chemistry)</span></span>

<span data-ttu-id="f8cab-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="f8cab-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="f8cab-105">Klassischer Verarbeitungsschritt von `ApplyDeltaParity` .</span><span class="sxs-lookup"><span data-stu-id="f8cab-105">Classical processing step of `ApplyDeltaParity`.</span></span>
<span data-ttu-id="f8cab-106">Dadurch wird eine Liste von Steuerungs-Qubits zum Auswerten der Paritäts Unterschiede zwischen zwei pqrs berechnet... Begriffe der geraden Länge.</span><span class="sxs-lookup"><span data-stu-id="f8cab-106">This computes a list of control qubits for evaluating parity difference between any two PQRS... terms of even length.</span></span>

```qsharp
function _DeltaParityCNOTbitstring (prevFermionicTerm : Int[], nextFermionicTerm : Int[]) : (Int, Bool[])
```


## <a name="input"></a><span data-ttu-id="f8cab-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f8cab-107">Input</span></span>

### <a name="prevfermionicterm--int"></a><span data-ttu-id="f8cab-108">prevfermionicterm: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="f8cab-108">prevFermionicTerm : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>




### <a name="nextfermionicterm--int"></a><span data-ttu-id="f8cab-109">nextfermionicterm: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="f8cab-109">nextFermionicTerm : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>





## <a name="output--intbool"></a><span data-ttu-id="f8cab-110">Ausgabe: ([int](xref:microsoft.quantum.lang-ref.int),[bool](xref:microsoft.quantum.lang-ref.bool)[])</span><span class="sxs-lookup"><span data-stu-id="f8cab-110">Output : ([Int](xref:microsoft.quantum.lang-ref.int),[Bool](xref:microsoft.quantum.lang-ref.bool)[])</span></span>



## <a name="remarks"></a><span data-ttu-id="f8cab-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f8cab-111">Remarks</span></span>

<span data-ttu-id="f8cab-112">Dabei wird davon ausgegangen, dass die Länge der Begriffe gleich ist.</span><span class="sxs-lookup"><span data-stu-id="f8cab-112">This assumes that the length of terms is even.</span></span>
<span data-ttu-id="f8cab-113">Berechnet die Liste der Steuerelemente für den Paritäts Unterschied zwischen zwei Begriffen.</span><span class="sxs-lookup"><span data-stu-id="f8cab-113">Computes list of controls for parity difference between any two terms.</span></span>
<span data-ttu-id="f8cab-114">Dabei wird davon ausgegangen, dass die Eingabe Listen in aufsteigender Reihenfolge sortiert sind.</span><span class="sxs-lookup"><span data-stu-id="f8cab-114">This assumes that the input lists is sorted in ascending order.</span></span>