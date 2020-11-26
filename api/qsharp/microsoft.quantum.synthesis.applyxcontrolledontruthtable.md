---
uid: Microsoft.Quantum.Synthesis.ApplyXControlledOnTruthTable
title: Applyxcontrolledontruthtable-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: ApplyXControlledOnTruthTable
qsharp.summary: Applies the @"microsoft.quantum.intrinsic.x" operation on `target`, if the Boolean function `func` evaluates to true for the classical assignment in `controlRegister`.
ms.openlocfilehash: aa4e1bc0d5058228721728a894b896331ec626d1
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96203296"
---
# <a name="applyxcontrolledontruthtable-operation"></a><span data-ttu-id="bab6c-102">Applyxcontrolledontruthtable-Vorgang</span><span class="sxs-lookup"><span data-stu-id="bab6c-102">ApplyXControlledOnTruthTable operation</span></span>

<span data-ttu-id="bab6c-103">Namespace: [Microsoft. Quantum. Synthese](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="bab6c-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="bab6c-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="bab6c-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="bab6c-105">Wendet den @"microsoft.quantum.intrinsic.x" Vorgang auf an `target` , wenn die boolesche Funktion `func` für die klassische Zuweisung in als true ausgewertet wird `controlRegister` .</span><span class="sxs-lookup"><span data-stu-id="bab6c-105">Applies the @"microsoft.quantum.intrinsic.x" operation on `target`, if the Boolean function `func` evaluates to true for the classical assignment in `controlRegister`.</span></span>

```qsharp
operation ApplyXControlledOnTruthTable (func : BigInt, controlRegister : Qubit[], target : Qubit) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="bab6c-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bab6c-106">Description</span></span>

<span data-ttu-id="bab6c-107">Der Vorgang implementiert den einheitlichen Vorgang \begin{align} u\ket {x} \ Ket {y} = \ket{x}\ket{y \oplus f (x)} \end{align}, wobei $x $ und $y $ `controlRegister` `target` bzw. darstellen.</span><span class="sxs-lookup"><span data-stu-id="bab6c-107">The operation implements the unitary operation \begin{align} U\ket{x}\ket{y} = \ket{x}\ket{y \oplus f(x)} \end{align} where $x$ and $y$ represent `controlRegister` and `target`, respectively.</span></span>

<span data-ttu-id="bab6c-108">Die boolesche Funktion $f $ wird als Wahrheitstabelle in Bezug auf eine große ganze Zahl dargestellt.</span><span class="sxs-lookup"><span data-stu-id="bab6c-108">The Boolean function $f$ is represented as a truth table in terms of a big integer.</span></span>
<span data-ttu-id="bab6c-109">Beispielsweise wird die Mehrheits Funktion für drei Eingaben durch das bitstring dargestellt `11101000` , wobei das signifikanteste Bit `1` der Eingabe Zuweisung entspricht `(1, 1, 1)` , und das am wenigsten bedeutende Bit `0` entspricht der Eingabe Zuweisung `(0, 0, 0)` .</span><span class="sxs-lookup"><span data-stu-id="bab6c-109">For example, the majority function on three inputs is represented by the bitstring `11101000`, where the most significant bit `1` corresponds to the input assignment `(1, 1, 1)`, and the least significant bit `0` corresponds to the input assignment `(0, 0, 0)`.</span></span>
<span data-ttu-id="bab6c-110">Sie kann durch die große ganze Zahl `0xE8L` in Hexadezimal Schreibweise oder als Dezimal Schreibweise dargestellt werden `232L` .</span><span class="sxs-lookup"><span data-stu-id="bab6c-110">It can be represented by the big integer `0xE8L` in hexadecimal notation or as `232L` in decimal notation.</span></span>  <span data-ttu-id="bab6c-111">Das- `L` Suffix gibt an, dass die Konstante vom Typ ist `BigInt` .</span><span class="sxs-lookup"><span data-stu-id="bab6c-111">The `L` suffix indicates that the constant is of type `BigInt`.</span></span>
<span data-ttu-id="bab6c-112">Weitere Informationen zu dieser Darstellung finden Sie auch in den [Wahrheitstabellen Kata](https://github.com/microsoft/QuantumKatas/tree/main/TruthTables).</span><span class="sxs-lookup"><span data-stu-id="bab6c-112">More details on this representation can also be found in the [truth tables kata](https://github.com/microsoft/QuantumKatas/tree/main/TruthTables).</span></span>

<span data-ttu-id="bab6c-113">Die-Implementierung nutzt @"microsoft.quantum.intrinsic.cnot" und @"microsoft.quantum.intrinsic.r1" Gates.</span><span class="sxs-lookup"><span data-stu-id="bab6c-113">The implementation makes use of @"microsoft.quantum.intrinsic.cnot" and @"microsoft.quantum.intrinsic.r1" gates.</span></span>

## <a name="input"></a><span data-ttu-id="bab6c-114">Eingabe</span><span class="sxs-lookup"><span data-stu-id="bab6c-114">Input</span></span>

### <a name="func--bigint"></a><span data-ttu-id="bab6c-115">Func: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="bab6c-115">func : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="bab6c-116">Boolesche Wahrheitstabelle, dargestellt als große ganze Zahl</span><span class="sxs-lookup"><span data-stu-id="bab6c-116">Boolean truth table represented as big integer</span></span>


### <a name="controlregister--qubit"></a><span data-ttu-id="bab6c-117">controlregister: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="bab6c-117">controlRegister : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="bab6c-118">Register von Steuerungs Qubits</span><span class="sxs-lookup"><span data-stu-id="bab6c-118">Register of control qubits</span></span>


### <a name="target--qubit"></a><span data-ttu-id="bab6c-119">Ziel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="bab6c-119">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="bab6c-120">Ziel-Qubit</span><span class="sxs-lookup"><span data-stu-id="bab6c-120">Target qubit</span></span>



## <a name="output--unit"></a><span data-ttu-id="bab6c-121">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="bab6c-121">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="references"></a><span data-ttu-id="bab6c-122">Referenzen</span><span class="sxs-lookup"><span data-stu-id="bab6c-122">References</span></span>

- [<span data-ttu-id="bab6c-123">*N. Schuch*, *J. Siewert*, PRL 91, No. 027902, 2003, arXiv: quant-ph/0303063</span><span class="sxs-lookup"><span data-stu-id="bab6c-123">*N. Schuch*, *J. Siewert*, PRL 91, no. 027902, 2003, arXiv:quant-ph/0303063</span></span>](https://arxiv.org/abs/quant-ph/0303063)
- [<span data-ttu-id="bab6c-124">*Mathias soeken*, *Martin roetteler*, arXiv: 2005.12310</span><span class="sxs-lookup"><span data-stu-id="bab6c-124">*Mathias Soeken*, *Martin Roetteler*, arXiv:2005.12310</span></span>](https://arxiv.org/abs/2005.12310)

## <a name="see-also"></a><span data-ttu-id="bab6c-125">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="bab6c-125">See Also</span></span>

- [<span data-ttu-id="bab6c-126">Microsoft. Quantum. Synthese. applyxcontrolledontruthtablewithcleantarget</span><span class="sxs-lookup"><span data-stu-id="bab6c-126">Microsoft.Quantum.Synthesis.ApplyXControlledOnTruthTableWithCleanTarget</span></span>](xref:Microsoft.Quantum.Synthesis.ApplyXControlledOnTruthTableWithCleanTarget)