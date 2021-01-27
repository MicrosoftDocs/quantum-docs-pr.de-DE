---
uid: Microsoft.Quantum.Chemistry.JordanWigner._ComputeJordanWignerBitString
title: _ComputeJordanWignerBitString-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: _ComputeJordanWignerBitString
qsharp.summary: Computes Z component of Jordan–Wigner string between fermion indices in a fermionic operator with an even number of creation / annihilation operators.
ms.openlocfilehash: 82b5e433f79c93c640b89e6365e5f468bacd892e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98839524"
---
# <a name="_computejordanwignerbitstring-function"></a><span data-ttu-id="a4135-102">_ComputeJordanWignerBitString-Funktion</span><span class="sxs-lookup"><span data-stu-id="a4135-102">_ComputeJordanWignerBitString function</span></span>

<span data-ttu-id="a4135-103">Namespace: [Microsoft. Quantum. Chemistry. jordanwigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="a4135-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="a4135-104">Paket: [Microsoft. Quantum. Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="a4135-104">Package: [Microsoft.Quantum.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span></span>


<span data-ttu-id="a4135-105">Berechnet die Z-Komponente von Jordanien – Wigner-Zeichenfolge zwischen Fermion-Indizes in einem fermionic-Operator mit einer geraden Anzahl von Erstellungs-/Vernichtungs Operatoren.</span><span class="sxs-lookup"><span data-stu-id="a4135-105">Computes Z component of Jordan–Wigner string between fermion indices in a fermionic operator with an even number of creation / annihilation operators.</span></span>

```qsharp
function _ComputeJordanWignerBitString (nFermions : Int, idxFermions : Int[]) : Bool[]
```


## <a name="input"></a><span data-ttu-id="a4135-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a4135-106">Input</span></span>

### <a name="nfermions--int"></a><span data-ttu-id="a4135-107">nfermions: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="a4135-107">nFermions : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="a4135-108">Die Anzahl der Fermionen im System.</span><span class="sxs-lookup"><span data-stu-id="a4135-108">The Number of fermions in the system.</span></span>


### <a name="idxfermions--int"></a><span data-ttu-id="a4135-109">idxfermions: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="a4135-109">idxFermions : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="a4135-110">fermionic-Operator Indizes.</span><span class="sxs-lookup"><span data-stu-id="a4135-110">fermionic operator indices.</span></span>



## <a name="output--bool"></a><span data-ttu-id="a4135-111">Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)[]</span><span class="sxs-lookup"><span data-stu-id="a4135-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span></span>

<span data-ttu-id="a4135-112">Bitzeichenfolge `Bool[]` , auf die `true` ein `PauliZ` angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a4135-112">Bitstring `Bool[]` that is `true` where a `PauliZ` should be applied.</span></span>

## <a name="example"></a><span data-ttu-id="a4135-113">Beispiel</span><span class="sxs-lookup"><span data-stu-id="a4135-113">Example</span></span>

<span data-ttu-id="a4135-114">Let bitstring = _ComputeJordanWignerBitString (6, [0, 1, 2, 6]); bitstring ist [false, false, false, true, true, true, false].</span><span class="sxs-lookup"><span data-stu-id="a4135-114">let bitString = _ComputeJordanWignerBitString(6, [0,1,2,6]) ; // bitString is [false, false, false ,true, true, true, false].</span></span>