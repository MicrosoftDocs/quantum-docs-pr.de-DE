---
uid: Microsoft.Quantum.Simulation.BlockEncodingToReflection
title: Blockencodingtoreflection-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: BlockEncodingToReflection
qsharp.summary: >-
  Converts a `BlockEncoding` into an equivalent `BLockEncodingReflection`.

  That is, given a `BlockEncoding` unitary $U$ that encodes some operator $H$ of interest, converts it into a `BlockEncodingReflection` $U'$ that encodes the same operator, but also satisfies $U'^\dagger = U'$. This increases the size of the auxiliary register of $U$ by one qubit.
ms.openlocfilehash: a8b4c65f8c32f7f9185f1dbdacf8fc75fd4573b1
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92722066"
---
# <a name="blockencodingtoreflection-function"></a><span data-ttu-id="e27b1-102">Blockencodingtoreflection-Funktion</span><span class="sxs-lookup"><span data-stu-id="e27b1-102">BlockEncodingToReflection function</span></span>

<span data-ttu-id="e27b1-103">Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="e27b1-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="e27b1-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="e27b1-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="e27b1-105">Konvertiert einen `BlockEncoding` in eine-Entsprechung `BLockEncodingReflection` .</span><span class="sxs-lookup"><span data-stu-id="e27b1-105">Converts a `BlockEncoding` into an equivalent `BLockEncodingReflection`.</span></span>

<span data-ttu-id="e27b1-106">Das heißt, bei einem `BlockEncoding` einheitlichen $U $, der einen Operator $H $ of Interest codiert, konvertiert ihn in eine `BlockEncodingReflection` $U ' $, die denselben Operator codiert, aber auch $U ' ^ \dagger = U ' $ entspricht.</span><span class="sxs-lookup"><span data-stu-id="e27b1-106">That is, given a `BlockEncoding` unitary $U$ that encodes some operator $H$ of interest, converts it into a `BlockEncodingReflection` $U'$ that encodes the same operator, but also satisfies $U'^\dagger = U'$.</span></span>
<span data-ttu-id="e27b1-107">Dadurch wird die Größe des zusätzlichen Registers $U $ um ein Qubit vergrößert.</span><span class="sxs-lookup"><span data-stu-id="e27b1-107">This increases the size of the auxiliary register of $U$ by one qubit.</span></span>

```qsharp
function BlockEncodingToReflection (blockEncoding : Microsoft.Quantum.Simulation.BlockEncoding) : Microsoft.Quantum.Simulation.BlockEncodingReflection
```


## <a name="input"></a><span data-ttu-id="e27b1-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e27b1-108">Input</span></span>

### <a name="blockencoding--blockencoding"></a><span data-ttu-id="e27b1-109">blockencoding: [blockencoding](xref:Microsoft.Quantum.Simulation.BlockEncoding)</span><span class="sxs-lookup"><span data-stu-id="e27b1-109">blockEncoding : [BlockEncoding](xref:Microsoft.Quantum.Simulation.BlockEncoding)</span></span>

<span data-ttu-id="e27b1-110">Ein `BlockEncoding` einheitlicher $U $, der in eine Reflektion konvertiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="e27b1-110">A `BlockEncoding` unitary $U$ to be converted into a reflection.</span></span>



## <a name="output--blockencodingreflection"></a><span data-ttu-id="e27b1-111">Ausgabe: [blockencodingreflection](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection)</span><span class="sxs-lookup"><span data-stu-id="e27b1-111">Output : [BlockEncodingReflection](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection)</span></span>

<span data-ttu-id="e27b1-112">Ein einheitlicher $U ' $, der sich zusammen für Register registriert `a` und `s` $H $ codiert und $U ' ^ \dagger = U ' $ entspricht.</span><span class="sxs-lookup"><span data-stu-id="e27b1-112">A unitary $U'$ acting jointly on registers `a` and `s` that block- encodes $H$, and satisfies $U'^\dagger = U'$.</span></span>

## <a name="remarks"></a><span data-ttu-id="e27b1-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e27b1-113">Remarks</span></span>

<span data-ttu-id="e27b1-114">Dadurch wird die Größe des zusätzlichen Registers $U $ um ein Qubit vergrößert.</span><span class="sxs-lookup"><span data-stu-id="e27b1-114">This increases the size of the auxiliary register of $U$ by one qubit.</span></span>

## <a name="references"></a><span data-ttu-id="e27b1-115">Referenzen</span><span class="sxs-lookup"><span data-stu-id="e27b1-115">References</span></span>

- <span data-ttu-id="e27b1-116">Hamiltona Simulation by qubitisierung Guang Hao Low, ISAL. Chuang https://arxiv.org/abs/1610.06546</span><span class="sxs-lookup"><span data-stu-id="e27b1-116">Hamiltonian Simulation by Qubitization Guang Hao Low, Isaac L. Chuang https://arxiv.org/abs/1610.06546</span></span>

## <a name="see-also"></a><span data-ttu-id="e27b1-117">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e27b1-117">See Also</span></span>

- [<span data-ttu-id="e27b1-118">Microsoft. Quantum. Simulation. blockencoding</span><span class="sxs-lookup"><span data-stu-id="e27b1-118">Microsoft.Quantum.Simulation.BlockEncoding</span></span>](xref:Microsoft.Quantum.Simulation.BlockEncoding)
- [<span data-ttu-id="e27b1-119">Microsoft. Quantum. Simulation. blockencodingreflection</span><span class="sxs-lookup"><span data-stu-id="e27b1-119">Microsoft.Quantum.Simulation.BlockEncodingReflection</span></span>](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection)