---
uid: Microsoft.Quantum.Arithmetic.IncrementPhaseByInteger
title: Incrementphasebyinteger-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: IncrementPhaseByInteger
qsharp.summary: Increments an unsigned quantum register by a classical integer, using phase rotations.
ms.openlocfilehash: fb67455dadbc7a2f38880581f0e413a747faa8ef
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707247"
---
# <a name="incrementphasebyinteger-operation"></a><span data-ttu-id="100d2-102">Incrementphasebyinteger-Vorgang</span><span class="sxs-lookup"><span data-stu-id="100d2-102">IncrementPhaseByInteger operation</span></span>

<span data-ttu-id="100d2-103">Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="100d2-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="100d2-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="100d2-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="100d2-105">Erhöht mithilfe von Phasen Drehungen ein unsigniertes Quantum-Register durch eine klassische Ganzzahl.</span><span class="sxs-lookup"><span data-stu-id="100d2-105">Increments an unsigned quantum register by a classical integer, using phase rotations.</span></span>

```qsharp
operation IncrementPhaseByInteger (increment : Int, target : Microsoft.Quantum.Arithmetic.PhaseLittleEndian) : Unit
```


## <a name="description"></a><span data-ttu-id="100d2-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="100d2-106">Description</span></span>

<span data-ttu-id="100d2-107">Angenommen, das `target` codiert eine Ganzzahl ohne Vorzeichen $x $ in einer Little-in-codiercodierung und `increment` ist gleich $a $.</span><span class="sxs-lookup"><span data-stu-id="100d2-107">Suppose that `target` encodes an unsigned integer $x$ in a little-endian encoding and that `increment` is equal to $a$.</span></span>
<span data-ttu-id="100d2-108">Anschließend implementiert dieser Vorgang die einheitliche $ \ket{x} \mapsto \ket{x + a} $, wobei die Addition Modulo $2 ^ n $ ist, wobei $n = \texttt{length (Target!)} $.</span><span class="sxs-lookup"><span data-stu-id="100d2-108">Then, this operation implements the unitary $\ket{x} \mapsto \ket{x + a}$, where the addition is performed modulo $2^n$, where $n = \texttt{Length(target!)}$.</span></span>

## <a name="input"></a><span data-ttu-id="100d2-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="100d2-109">Input</span></span>

### <a name="increment--int"></a><span data-ttu-id="100d2-110">Inkrement: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="100d2-110">increment : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="100d2-111">Die ganze Zahl, um die die `target` inkrementiert wird.</span><span class="sxs-lookup"><span data-stu-id="100d2-111">The integer by which the `target` is incremented by.</span></span>


### <a name="target--phaselittleendian"></a><span data-ttu-id="100d2-112">Ziel: [phaselittleenddian](xref:Microsoft.Quantum.Arithmetic.PhaseLittleEndian)</span><span class="sxs-lookup"><span data-stu-id="100d2-112">target : [PhaseLittleEndian](xref:Microsoft.Quantum.Arithmetic.PhaseLittleEndian)</span></span>

<span data-ttu-id="100d2-113">Ein Quantum-Register codiert eine Ganzzahl ohne Vorzeichen unter Verwendung der Little-d-Codierung in der Dual (QFT)-Basis.</span><span class="sxs-lookup"><span data-stu-id="100d2-113">A quantum register encoding an unsigned integer using little-endian encoding in the dual (QFT) basis.</span></span>



## <a name="output--unit"></a><span data-ttu-id="100d2-114">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="100d2-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="100d2-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="100d2-115">Remarks</span></span>

<span data-ttu-id="100d2-116">Beachten Sie, dass wir die Verbindung vereinfacht haben, da das Inkrement eine klassische Konstante und kein Quantum-Register ist.</span><span class="sxs-lookup"><span data-stu-id="100d2-116">Note that we have simplified the circuit because the increment is a classical constant, not a quantum register.</span></span>

<span data-ttu-id="100d2-117">Ein Leitungs Diagramm und eine Erläuterung finden Sie in der Abbildung auf der [ Seite 6 von arXiv: quant-ph/0008033v1 ](https://arxiv.org/pdf/quant-ph/0008033.pdf#page=6) .</span><span class="sxs-lookup"><span data-stu-id="100d2-117">See the figure on [ Page 6 of arXiv:quant-ph/0008033v1 ](https://arxiv.org/pdf/quant-ph/0008033.pdf#page=6) for the circuit diagram and explanation.</span></span>

## <a name="references"></a><span data-ttu-id="100d2-118">Referenzen</span><span class="sxs-lookup"><span data-stu-id="100d2-118">References</span></span>

- [<span data-ttu-id="100d2-119">*Thomas G. Draper* , arXiv: quant-ph/0008033</span><span class="sxs-lookup"><span data-stu-id="100d2-119"> *Thomas G. Draper* , arXiv:quant-ph/0008033</span></span>](https://arxiv.org/pdf/quant-ph/0008033v1.pdf)

## <a name="see-also"></a><span data-ttu-id="100d2-120">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="100d2-120">See Also</span></span>

- [<span data-ttu-id="100d2-121">Microsoft. Quantum. Arithmetik. incrementbyinteger</span><span class="sxs-lookup"><span data-stu-id="100d2-121">Microsoft.Quantum.Arithmetic.IncrementByInteger</span></span>](xref:Microsoft.Quantum.Arithmetic.IncrementByInteger)