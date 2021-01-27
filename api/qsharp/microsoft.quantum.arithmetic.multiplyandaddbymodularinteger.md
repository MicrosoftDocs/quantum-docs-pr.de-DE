---
uid: Microsoft.Quantum.Arithmetic.MultiplyAndAddByModularInteger
title: Multiplyandaddbymodularinteger-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: MultiplyAndAddByModularInteger
qsharp.summary: Performs a modular multiply-and-add by integer constants on a qubit register.
ms.openlocfilehash: e4de934a5776e80dbf5f0d8334bf806e6a84b743
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846514"
---
# <a name="multiplyandaddbymodularinteger-operation"></a><span data-ttu-id="00cf4-102">Multiplyandaddbymodularinteger-Vorgang</span><span class="sxs-lookup"><span data-stu-id="00cf4-102">MultiplyAndAddByModularInteger operation</span></span>

<span data-ttu-id="00cf4-103">Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="00cf4-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="00cf4-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="00cf4-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="00cf4-105">Führt einen modularen Multiplikations-und-Add by integer-Konstanten für ein Qubit-Register aus.</span><span class="sxs-lookup"><span data-stu-id="00cf4-105">Performs a modular multiply-and-add by integer constants on a qubit register.</span></span>

```qsharp
operation MultiplyAndAddByModularInteger (constMultiplier : Int, modulus : Int, multiplier : Microsoft.Quantum.Arithmetic.LittleEndian, summand : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="00cf4-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="00cf4-106">Description</span></span>

<span data-ttu-id="00cf4-107">Implementiert die Zuordnung $ $ \begin{align} \ket{x} \ket{b} \mapsto \ket{x} \ket{(b + a \cdot x) \operatschmue{mod} N} \end{align} $ $ für einen angegebenen Modulo $N $, Konstanten Multiplikator $a $ und sumand $y $.</span><span class="sxs-lookup"><span data-stu-id="00cf4-107">Implements the map $$ \begin{align} \ket{x} \ket{b} \mapsto \ket{x} \ket{(b + a \cdot x) \operatorname{mod} N} \end{align} $$ for a given modulus $N$, constant multiplier $a$, and summand $y$.</span></span>

## <a name="input"></a><span data-ttu-id="00cf4-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="00cf4-108">Input</span></span>

### <a name="constmultiplier--int"></a><span data-ttu-id="00cf4-109">constmultiplikator: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="00cf4-109">constMultiplier : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="00cf4-110">Eine ganze Zahl $a $, die jeder Basis Zustands Bezeichnung hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="00cf4-110">An integer $a$ to be added to each basis state label.</span></span>


### <a name="modulus--int"></a><span data-ttu-id="00cf4-111">Modulo: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="00cf4-111">modulus : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="00cf4-112">Der Modulo $N $, bei dem Addition und Multiplikation in Bezug auf übernommen werden.</span><span class="sxs-lookup"><span data-stu-id="00cf4-112">The modulus $N$ which addition and multiplication is taken with respect to.</span></span>


### <a name="multiplier--littleendian"></a><span data-ttu-id="00cf4-113">Multiplikator: [littleenddian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="00cf4-113">multiplier : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="00cf4-114">Ein Quantum-Register, das eine Ganzzahl ohne Vorzeichen darstellt, deren Wert jeder Basis Zustands Bezeichnung von hinzugefügt werden soll `summand` .</span><span class="sxs-lookup"><span data-stu-id="00cf4-114">A quantum register representing an unsigned integer whose value is to be added to each basis state label of `summand`.</span></span>


### <a name="summand--littleendian"></a><span data-ttu-id="00cf4-115">sumand: [littleddian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="00cf4-115">summand : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="00cf4-116">Ein Quantum-Register, das eine Ganzzahl ohne Vorzeichen darstellt, die als Ziel für diesen Vorgang verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="00cf4-116">A quantum register representing an unsigned integer to use as the target for this operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="00cf4-117">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="00cf4-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="00cf4-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="00cf4-118">Remarks</span></span>

- <span data-ttu-id="00cf4-119">Ein Leit Diagramm und eine Erläuterung finden Sie in Abbildung 6 auf [Seite 7 von arXiv: quant-ph/0205095v3](https://arxiv.org/pdf/quant-ph/0205095v3.pdf#page=7)</span><span class="sxs-lookup"><span data-stu-id="00cf4-119">For the circuit diagram and explanation see Figure 6 on [Page 7 of arXiv:quant-ph/0205095v3](https://arxiv.org/pdf/quant-ph/0205095v3.pdf#page=7)</span></span>
- <span data-ttu-id="00cf4-120">Dieser Vorgang entspricht cmult (a) mod (N) in [arXiv: quant-ph/0205095v3](https://arxiv.org/pdf/quant-ph/0205095v3.pdf)</span><span class="sxs-lookup"><span data-stu-id="00cf4-120">This operation corresponds to CMULT(a)MOD(N) in [arXiv:quant-ph/0205095v3](https://arxiv.org/pdf/quant-ph/0205095v3.pdf)</span></span>

## <a name="see-also"></a><span data-ttu-id="00cf4-121">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="00cf4-121">See Also</span></span>

- [<span data-ttu-id="00cf4-122">Microsoft. Quantum. Arithmetik. multiplyandaddphasebymodularinteger</span><span class="sxs-lookup"><span data-stu-id="00cf4-122">Microsoft.Quantum.Arithmetic.MultiplyAndAddPhaseByModularInteger</span></span>](xref:Microsoft.Quantum.Arithmetic.MultiplyAndAddPhaseByModularInteger)