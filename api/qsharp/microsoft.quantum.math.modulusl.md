---
uid: Microsoft.Quantum.Math.ModulusL
title: Modulusl-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ModulusL
qsharp.summary: Computes the canonical residue of `value` modulo `modulus`.
ms.openlocfilehash: 6be2edb052cf55f8e8465c76b5dcadeb61ff11ea
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842744"
---
# <a name="modulusl-function"></a><span data-ttu-id="ca46f-102">Modulusl-Funktion</span><span class="sxs-lookup"><span data-stu-id="ca46f-102">ModulusL function</span></span>

<span data-ttu-id="ca46f-103">Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="ca46f-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="ca46f-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="ca46f-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="ca46f-105">Berechnet den kanonischen Rückstand von `value` Modulo `modulus` .</span><span class="sxs-lookup"><span data-stu-id="ca46f-105">Computes the canonical residue of `value` modulo `modulus`.</span></span>

```qsharp
function ModulusL (value : BigInt, modulus : BigInt) : BigInt
```


## <a name="input"></a><span data-ttu-id="ca46f-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ca46f-106">Input</span></span>

### <a name="value--bigint"></a><span data-ttu-id="ca46f-107">Wert: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="ca46f-107">value : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="ca46f-108">Der Wert, von dem die Rückstände berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="ca46f-108">The value of which residue is computed</span></span>


### <a name="modulus--bigint"></a><span data-ttu-id="ca46f-109">Modulo: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="ca46f-109">modulus : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="ca46f-110">Der Modulo, nach dem die Rückstände übernommen werden, muss positiv sein.</span><span class="sxs-lookup"><span data-stu-id="ca46f-110">The modulus by which residues are take, must be positive</span></span>



## <a name="output--bigint"></a><span data-ttu-id="ca46f-111">Ausgabe: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="ca46f-111">Output : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="ca46f-112">Ganzzahliger $r $ zwischen 0 und `modulus - 1` so, dass `value - r` durch Modulo teilbar ist</span><span class="sxs-lookup"><span data-stu-id="ca46f-112">Integer $r$ between 0 and `modulus - 1` such that `value - r` is divisible by modulus</span></span>

## <a name="remarks"></a><span data-ttu-id="ca46f-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ca46f-113">Remarks</span></span>

<span data-ttu-id="ca46f-114">Diese Funktion verhält sich unterschiedlich, wie sich der Operator `%` in c# verhält, und f #, da im Ergebnis immer eine nicht negative ganze Zahl zwischen 0 und ist `modulus - 1` , auch wenn der Wert negativ ist.</span><span class="sxs-lookup"><span data-stu-id="ca46f-114">This function behaves different to how the operator `%` behaves in C# and Q# as in the result is always a non-negative integer between 0 and `modulus - 1`, even if value is negative.</span></span>