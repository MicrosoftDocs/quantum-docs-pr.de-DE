---
uid: Microsoft.Quantum.Arithmetic.MultiplyAndAddByModularInteger
title: Multiplyandaddbymodularinteger-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: MultiplyAndAddByModularInteger
qsharp.summary: Performs a modular multiply-and-add by integer constants on a qubit register.
ms.openlocfilehash: 169326879919b5b72d600c33d624776b720cc6bc
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96222591"
---
# <a name="multiplyandaddbymodularinteger-operation"></a><span data-ttu-id="a26d6-102">Multiplyandaddbymodularinteger-Vorgang</span><span class="sxs-lookup"><span data-stu-id="a26d6-102">MultiplyAndAddByModularInteger operation</span></span>

<span data-ttu-id="a26d6-103">Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="a26d6-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="a26d6-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a26d6-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="a26d6-105">Führt einen modularen Multiplikations-und-Add by integer-Konstanten für ein Qubit-Register aus.</span><span class="sxs-lookup"><span data-stu-id="a26d6-105">Performs a modular multiply-and-add by integer constants on a qubit register.</span></span>

```qsharp
operation MultiplyAndAddByModularInteger (constMultiplier : Int, modulus : Int, multiplier : Microsoft.Quantum.Arithmetic.LittleEndian, summand : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="a26d6-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a26d6-106">Description</span></span>

<span data-ttu-id="a26d6-107">Implementiert die Zuordnung $ $ \begin{align} \ket{x} \ket{b} \mapsto \ket{x} \ket{(b + a \cdot x) \operatschmue{mod} N} \end{align} $ $ für einen angegebenen Modulo $N $, Konstanten Multiplikator $a $ und sumand $y $.</span><span class="sxs-lookup"><span data-stu-id="a26d6-107">Implements the map $$ \begin{align} \ket{x} \ket{b} \mapsto \ket{x} \ket{(b + a \cdot x) \operatorname{mod} N} \end{align} $$ for a given modulus $N$, constant multiplier $a$, and summand $y$.</span></span>

## <a name="input"></a><span data-ttu-id="a26d6-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a26d6-108">Input</span></span>

### <a name="constmultiplier--int"></a><span data-ttu-id="a26d6-109">constmultiplikator: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="a26d6-109">constMultiplier : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="a26d6-110">Eine ganze Zahl $a $, die jeder Basis Zustands Bezeichnung hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a26d6-110">An integer $a$ to be added to each basis state label.</span></span>


### <a name="modulus--int"></a><span data-ttu-id="a26d6-111">Modulo: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="a26d6-111">modulus : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="a26d6-112">Der Modulo $N $, bei dem Addition und Multiplikation in Bezug auf übernommen werden.</span><span class="sxs-lookup"><span data-stu-id="a26d6-112">The modulus $N$ which addition and multiplication is taken with respect to.</span></span>


### <a name="multiplier--littleendian"></a><span data-ttu-id="a26d6-113">Multiplikator: [littleenddian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="a26d6-113">multiplier : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="a26d6-114">Ein Quantum-Register, das eine Ganzzahl ohne Vorzeichen darstellt, deren Wert jeder Basis Zustands Bezeichnung von hinzugefügt werden soll `summand` .</span><span class="sxs-lookup"><span data-stu-id="a26d6-114">A quantum register representing an unsigned integer whose value is to be added to each basis state label of `summand`.</span></span>


### <a name="summand--littleendian"></a><span data-ttu-id="a26d6-115">sumand: [littleddian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="a26d6-115">summand : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="a26d6-116">Ein Quantum-Register, das eine Ganzzahl ohne Vorzeichen darstellt, die als Ziel für diesen Vorgang verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a26d6-116">A quantum register representing an unsigned integer to use as the target for this operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="a26d6-117">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="a26d6-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="a26d6-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a26d6-118">Remarks</span></span>

- <span data-ttu-id="a26d6-119">Ein Leit Diagramm und eine Erläuterung finden Sie in Abbildung 6 auf [Seite 7 von arXiv: quant-ph/0205095v3](https://arxiv.org/pdf/quant-ph/0205095v3.pdf#page=7)</span><span class="sxs-lookup"><span data-stu-id="a26d6-119">For the circuit diagram and explanation see Figure 6 on [Page 7 of arXiv:quant-ph/0205095v3](https://arxiv.org/pdf/quant-ph/0205095v3.pdf#page=7)</span></span>
- <span data-ttu-id="a26d6-120">Dieser Vorgang entspricht cmult (a) mod (N) in [arXiv: quant-ph/0205095v3](https://arxiv.org/pdf/quant-ph/0205095v3.pdf)</span><span class="sxs-lookup"><span data-stu-id="a26d6-120">This operation corresponds to CMULT(a)MOD(N) in [arXiv:quant-ph/0205095v3](https://arxiv.org/pdf/quant-ph/0205095v3.pdf)</span></span>

## <a name="see-also"></a><span data-ttu-id="a26d6-121">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="a26d6-121">See Also</span></span>

- [<span data-ttu-id="a26d6-122">Microsoft. Quantum. Arithmetik. multiplyandaddphasebymodularinteger</span><span class="sxs-lookup"><span data-stu-id="a26d6-122">Microsoft.Quantum.Arithmetic.MultiplyAndAddPhaseByModularInteger</span></span>](xref:Microsoft.Quantum.Arithmetic.MultiplyAndAddPhaseByModularInteger)