---
uid: Microsoft.Quantum.Arithmetic.MultiplyAndAddPhaseByModularInteger
title: Multiplyandaddphasebymodularinteger-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: MultiplyAndAddPhaseByModularInteger
qsharp.summary: The same as MultiplyAndAddByModularInteger, but assumes that the summand encodes integers in QFT basis.
ms.openlocfilehash: b1214acc2cafc3fede9fcb6663a435c0b1d2cf4a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843065"
---
# <a name="multiplyandaddphasebymodularinteger-operation"></a><span data-ttu-id="3bab7-102">Multiplyandaddphasebymodularinteger-Vorgang</span><span class="sxs-lookup"><span data-stu-id="3bab7-102">MultiplyAndAddPhaseByModularInteger operation</span></span>

<span data-ttu-id="3bab7-103">Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="3bab7-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="3bab7-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="3bab7-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="3bab7-105">Das gleiche wie bei multiplyandaddbymodularinteger, jedoch wird davon ausgegangen, dass die Summen-und-Werte Ganzzahlen in QFT codieren.</span><span class="sxs-lookup"><span data-stu-id="3bab7-105">The same as MultiplyAndAddByModularInteger, but assumes that the summand encodes integers in QFT basis.</span></span>

```qsharp
operation MultiplyAndAddPhaseByModularInteger (constMultiplier : Int, modulus : Int, multiplier : Microsoft.Quantum.Arithmetic.LittleEndian, phaseSummand : Microsoft.Quantum.Arithmetic.PhaseLittleEndian) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="3bab7-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="3bab7-106">Input</span></span>

### <a name="constmultiplier--int"></a><span data-ttu-id="3bab7-107">constmultiplikator: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="3bab7-107">constMultiplier : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="3bab7-108">Eine ganze Zahl $a $, die jeder Basis Zustands Bezeichnung hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="3bab7-108">An integer $a$ to be added to each basis state label.</span></span>


### <a name="modulus--int"></a><span data-ttu-id="3bab7-109">Modulo: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="3bab7-109">modulus : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="3bab7-110">Der Modulo $N $, bei dem Addition und Multiplikation in Bezug auf übernommen werden.</span><span class="sxs-lookup"><span data-stu-id="3bab7-110">The modulus $N$ which addition and multiplication is taken with respect to.</span></span>


### <a name="multiplier--littleendian"></a><span data-ttu-id="3bab7-111">Multiplikator: [littleenddian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="3bab7-111">multiplier : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="3bab7-112">Ein Quantum-Register, das eine Ganzzahl ohne Vorzeichen darstellt, deren Wert jeder Basis Zustands Bezeichnung von hinzugefügt werden soll `summand` .</span><span class="sxs-lookup"><span data-stu-id="3bab7-112">A quantum register representing an unsigned integer whose value is to be added to each basis state label of `summand`.</span></span>


### <a name="phasesummand--phaselittleendian"></a><span data-ttu-id="3bab7-113">phasesummand: [phaselittleendian](xref:Microsoft.Quantum.Arithmetic.PhaseLittleEndian)</span><span class="sxs-lookup"><span data-stu-id="3bab7-113">phaseSummand : [PhaseLittleEndian](xref:Microsoft.Quantum.Arithmetic.PhaseLittleEndian)</span></span>

<span data-ttu-id="3bab7-114">Ein Quantum-Register, das eine Ganzzahl ohne Vorzeichen darstellt, die als Ziel für diesen Vorgang verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="3bab7-114">A quantum register representing an unsigned integer to use as the target for this operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="3bab7-115">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="3bab7-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="3bab7-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3bab7-116">Remarks</span></span>

<span data-ttu-id="3bab7-117">Geht davon aus, dass `phaseSummand` das höchste Bit auf 0 festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="3bab7-117">Assumes that `phaseSummand` has the highest bit set to 0.</span></span>
<span data-ttu-id="3bab7-118">Außerdem wird davon ausgegangen, dass der Wert von `phaseSummand` kleiner als $N $ ist.</span><span class="sxs-lookup"><span data-stu-id="3bab7-118">Also assumes that the value of `phaseSummand` is less than $N$.</span></span>

## <a name="see-also"></a><span data-ttu-id="3bab7-119">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="3bab7-119">See Also</span></span>

- [<span data-ttu-id="3bab7-120">Microsoft. Quantum. Arithmetik. multiplyandaddbymodularinteger</span><span class="sxs-lookup"><span data-stu-id="3bab7-120">Microsoft.Quantum.Arithmetic.MultiplyAndAddByModularInteger</span></span>](xref:Microsoft.Quantum.Arithmetic.MultiplyAndAddByModularInteger)