---
uid: Microsoft.Quantum.Chemistry.JordanWigner._ComputeJordanWignerBitString
title: _ComputeJordanWignerBitString-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: _ComputeJordanWignerBitString
qsharp.summary: Computes Z component of Jordan–Wigner string between fermion indices in a fermionic operator with an even number of creation / annihilation operators.
ms.openlocfilehash: 8121421a77174ef3e894381b281964b448e00a18
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96203942"
---
# <a name="_computejordanwignerbitstring-function"></a><span data-ttu-id="c02ef-102">_ComputeJordanWignerBitString-Funktion</span><span class="sxs-lookup"><span data-stu-id="c02ef-102">_ComputeJordanWignerBitString function</span></span>

<span data-ttu-id="c02ef-103">Namespace: [Microsoft. Quantum. Chemistry. jordanwigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="c02ef-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="c02ef-104">Paket: [Microsoft. Quantum. Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="c02ef-104">Package: [Microsoft.Quantum.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span></span>


<span data-ttu-id="c02ef-105">Berechnet die Z-Komponente von Jordanien – Wigner-Zeichenfolge zwischen Fermion-Indizes in einem fermionic-Operator mit einer geraden Anzahl von Erstellungs-/Vernichtungs Operatoren.</span><span class="sxs-lookup"><span data-stu-id="c02ef-105">Computes Z component of Jordan–Wigner string between fermion indices in a fermionic operator with an even number of creation / annihilation operators.</span></span>

```qsharp
function _ComputeJordanWignerBitString (nFermions : Int, idxFermions : Int[]) : Bool[]
```


## <a name="input"></a><span data-ttu-id="c02ef-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c02ef-106">Input</span></span>

### <a name="nfermions--int"></a><span data-ttu-id="c02ef-107">nfermions: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="c02ef-107">nFermions : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="c02ef-108">Die Anzahl der Fermionen im System.</span><span class="sxs-lookup"><span data-stu-id="c02ef-108">The Number of fermions in the system.</span></span>


### <a name="idxfermions--int"></a><span data-ttu-id="c02ef-109">idxfermions: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="c02ef-109">idxFermions : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="c02ef-110">fermionic-Operator Indizes.</span><span class="sxs-lookup"><span data-stu-id="c02ef-110">fermionic operator indices.</span></span>



## <a name="output--bool"></a><span data-ttu-id="c02ef-111">Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)[]</span><span class="sxs-lookup"><span data-stu-id="c02ef-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span></span>

<span data-ttu-id="c02ef-112">Bitzeichenfolge `Bool[]` , auf die `true` ein `PauliZ` angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c02ef-112">Bitstring `Bool[]` that is `true` where a `PauliZ` should be applied.</span></span>