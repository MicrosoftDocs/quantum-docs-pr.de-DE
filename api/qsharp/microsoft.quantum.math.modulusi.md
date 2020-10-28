---
uid: Microsoft.Quantum.Math.ModulusI
title: Modulusi-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ModulusI
qsharp.summary: Computes the canonical residue of `value` modulo `modulus`.
ms.openlocfilehash: 3f698a00b2c8d94b7cb3cca4f1721c659918f4a0
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92723088"
---
# <a name="modulusi-function"></a><span data-ttu-id="70c43-102">Modulusi-Funktion</span><span class="sxs-lookup"><span data-stu-id="70c43-102">ModulusI function</span></span>

<span data-ttu-id="70c43-103">Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="70c43-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="70c43-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="70c43-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="70c43-105">Berechnet den kanonischen Rückstand von `value` Modulo `modulus` .</span><span class="sxs-lookup"><span data-stu-id="70c43-105">Computes the canonical residue of `value` modulo `modulus`.</span></span>

```qsharp
function ModulusI (value : Int, modulus : Int) : Int
```


## <a name="input"></a><span data-ttu-id="70c43-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="70c43-106">Input</span></span>

### <a name="value--int"></a><span data-ttu-id="70c43-107">Wert: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="70c43-107">value : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="70c43-108">Der Wert, von dem die Rückstände berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="70c43-108">The value of which residue is computed</span></span>


### <a name="modulus--int"></a><span data-ttu-id="70c43-109">Modulo: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="70c43-109">modulus : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="70c43-110">Der Modulo, nach dem die Rückstände übernommen werden, muss positiv sein.</span><span class="sxs-lookup"><span data-stu-id="70c43-110">The modulus by which residues are take, must be positive</span></span>



## <a name="output--int"></a><span data-ttu-id="70c43-111">Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="70c43-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="70c43-112">Ganzzahliger $r $ zwischen 0 und `modulus - 1` so, dass `value - r` durch Modulo teilbar ist</span><span class="sxs-lookup"><span data-stu-id="70c43-112">Integer $r$ between 0 and `modulus - 1` such that `value - r` is divisible by modulus</span></span>

## <a name="remarks"></a><span data-ttu-id="70c43-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="70c43-113">Remarks</span></span>

<span data-ttu-id="70c43-114">Diese Funktion verhält sich unterschiedlich, wie sich der Operator `%` in c# verhält, und f #, da im Ergebnis immer eine positive ganze Zahl zwischen 0 und ist `modulus - 1` , auch wenn der Wert negativ ist.</span><span class="sxs-lookup"><span data-stu-id="70c43-114">This function behaves different to how the operator `%` behaves in C# and Q# as in the result is always a positive integer between 0 and `modulus - 1`, even if value is negative.</span></span>