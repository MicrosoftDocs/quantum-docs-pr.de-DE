---
uid: Microsoft.Quantum.Arithmetic.IncrementPhaseByModularInteger
title: Incrementphasebymodularinteger-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: IncrementPhaseByModularInteger
qsharp.summary: Performs a modular increment of a qubit register by an integer constant.
ms.openlocfilehash: 4ba35010d56ad01c73cb563646dc8150842da12e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846576"
---
# <a name="incrementphasebymodularinteger-operation"></a><span data-ttu-id="03d56-102">Incrementphasebymodularinteger-Vorgang</span><span class="sxs-lookup"><span data-stu-id="03d56-102">IncrementPhaseByModularInteger operation</span></span>

<span data-ttu-id="03d56-103">Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="03d56-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="03d56-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="03d56-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="03d56-105">Führt ein modulares Inkrement für ein Qubit-Register durch eine ganzzahlige Konstante aus.</span><span class="sxs-lookup"><span data-stu-id="03d56-105">Performs a modular increment of a qubit register by an integer constant.</span></span>

```qsharp
operation IncrementPhaseByModularInteger (increment : Int, modulus : Int, target : Microsoft.Quantum.Arithmetic.PhaseLittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="03d56-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="03d56-106">Description</span></span>

<span data-ttu-id="03d56-107">Geben Sie `increment` $a $ an, indem Sie `modulus` $N $ und Integer in `target` durch $y $ codiert haben.</span><span class="sxs-lookup"><span data-stu-id="03d56-107">Let us denote `increment` by $a$, `modulus` by $N$ and integer encoded in `target` by $y$.</span></span>
<span data-ttu-id="03d56-108">Anschließend führt der Vorgang die folgende Transformation aus: \begin{align} \ket{y} \mapsto \ket{(y + a) \operatorname{mod} N} \end{align} ganze Zahlen werden im Little-Endian-Format in QFT codiert.</span><span class="sxs-lookup"><span data-stu-id="03d56-108">Then the operation performs the following transformation: \begin{align} \ket{y} \mapsto \ket{(y + a) \operatorname{mod} N} \end{align} Integers are encoded in little-endian format in QFT basis.</span></span>

## <a name="input"></a><span data-ttu-id="03d56-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="03d56-109">Input</span></span>

### <a name="increment--int"></a><span data-ttu-id="03d56-110">Inkrement: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="03d56-110">increment : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="03d56-111">Ganzzahliges Inkrement $a $, das $y $ hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="03d56-111">Integer increment $a$ to be added to $y$.</span></span>


### <a name="modulus--int"></a><span data-ttu-id="03d56-112">Modulo: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="03d56-112">modulus : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="03d56-113">Ganzzahliger $N $, $y + a $.</span><span class="sxs-lookup"><span data-stu-id="03d56-113">Integer $N$ that mods $y + a$.</span></span>


### <a name="target--phaselittleendian"></a><span data-ttu-id="03d56-114">Ziel: [phaselittleenddian](xref:Microsoft.Quantum.Arithmetic.PhaseLittleEndian)</span><span class="sxs-lookup"><span data-stu-id="03d56-114">target : [PhaseLittleEndian](xref:Microsoft.Quantum.Arithmetic.PhaseLittleEndian)</span></span>

<span data-ttu-id="03d56-115">Ganzzahliger $y $ in Phasen codiertem Little-Endian-Format, dem `increment` $a $ hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="03d56-115">Integer $y$ in phase-encoded little-endian format that `increment` $a$ is added to.</span></span>



## <a name="output--unit"></a><span data-ttu-id="03d56-116">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="03d56-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="03d56-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="03d56-117">Remarks</span></span>

<span data-ttu-id="03d56-118">Geht davon aus, dass `target` das höchste Bit auf 0 festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="03d56-118">Assumes that `target` has the highest bit set to 0.</span></span>
<span data-ttu-id="03d56-119">Außerdem wird davon ausgegangen, dass der Wert von Target kleiner als $N $ ist.</span><span class="sxs-lookup"><span data-stu-id="03d56-119">Also assumes that the value of target is less than $N$.</span></span>

<span data-ttu-id="03d56-120">Das Verbindungs Diagramm und die Erläuterung finden Sie in Abbildung 5 auf [Seite 5 von arXiv: quant-ph/0205095v3](https://arxiv.org/pdf/quant-ph/0205095v3.pdf#page=5).</span><span class="sxs-lookup"><span data-stu-id="03d56-120">For the circuit diagram and explanation see Figure 5 on [Page 5 of arXiv:quant-ph/0205095v3](https://arxiv.org/pdf/quant-ph/0205095v3.pdf#page=5).</span></span>

## <a name="see-also"></a><span data-ttu-id="03d56-121">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="03d56-121">See Also</span></span>

- [<span data-ttu-id="03d56-122">Microsoft. Quantum. Arithmetik. incrementbymodularinteger</span><span class="sxs-lookup"><span data-stu-id="03d56-122">Microsoft.Quantum.Arithmetic.IncrementByModularInteger</span></span>](xref:Microsoft.Quantum.Arithmetic.IncrementByModularInteger)