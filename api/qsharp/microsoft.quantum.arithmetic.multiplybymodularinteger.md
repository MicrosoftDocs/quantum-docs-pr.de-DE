---
uid: Microsoft.Quantum.Arithmetic.MultiplyByModularInteger
title: Multiplybymodularinteger-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: MultiplyByModularInteger
qsharp.summary: Performs modular multiplication by an integer constant on a qubit register.
ms.openlocfilehash: bd4e0ad6c5bad779d9a31139690021fd9fcda210
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846495"
---
# <a name="multiplybymodularinteger-operation"></a><span data-ttu-id="57722-102">Multiplybymodularinteger-Vorgang</span><span class="sxs-lookup"><span data-stu-id="57722-102">MultiplyByModularInteger operation</span></span>

<span data-ttu-id="57722-103">Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="57722-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="57722-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="57722-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="57722-105">Führt eine modulare Multiplikation durch eine ganzzahlige Konstante in einem Qubit-Register durch.</span><span class="sxs-lookup"><span data-stu-id="57722-105">Performs modular multiplication by an integer constant on a qubit register.</span></span>

```qsharp
operation MultiplyByModularInteger (constMultiplier : Int, modulus : Int, multiplier : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="57722-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="57722-106">Description</span></span>

<span data-ttu-id="57722-107">Wir geben `modulus` $N $ und `constMultiplier` $a $ an.</span><span class="sxs-lookup"><span data-stu-id="57722-107">Let us denote `modulus` by $N$ and `constMultiplier` by $a$.</span></span>
<span data-ttu-id="57722-108">Durch diesen Vorgang wird ein einheitlicher Vorgang implementiert, der von der folgenden Karte auf der Berechnungsbasis definiert wird: $ $ \begin{align} \ket{y} \mapsto \ket{(a \cdot y) \operatschmue{mod} N} \end{align} $ $ für alle $y $ zwischen $0 $ und $N-$1.</span><span class="sxs-lookup"><span data-stu-id="57722-108">Then this operation implements a unitary operation defined by the following map on the computational basis: $$ \begin{align} \ket{y} \mapsto \ket{(a \cdot y) \operatorname{mod} N} \end{align} $$ for all $y$ between $0$ and $N - 1$.</span></span>

## <a name="input"></a><span data-ttu-id="57722-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="57722-109">Input</span></span>

### <a name="constmultiplier--int"></a><span data-ttu-id="57722-110">constmultiplikator: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="57722-110">constMultiplier : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="57722-111">Konstante, mit der der Multiplikator multipliziert wird.</span><span class="sxs-lookup"><span data-stu-id="57722-111">Constant by which multiplier is being multiplied.</span></span> <span data-ttu-id="57722-112">Muss eine Co-Primzahl sein, um Modulus zu geben.</span><span class="sxs-lookup"><span data-stu-id="57722-112">Must be co-prime to modulus.</span></span>


### <a name="modulus--int"></a><span data-ttu-id="57722-113">Modulo: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="57722-113">modulus : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="57722-114">Der Multiplikations Vorgang wird Modulo ausgeführt `modulus` .</span><span class="sxs-lookup"><span data-stu-id="57722-114">The multiplication operation is performed modulo `modulus`.</span></span>


### <a name="multiplier--littleendian"></a><span data-ttu-id="57722-115">Multiplikator: [littleenddian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="57722-115">multiplier : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="57722-116">Die Zahl, die mit einer Konstanten multipliziert wird.</span><span class="sxs-lookup"><span data-stu-id="57722-116">The number being multiplied by a constant.</span></span>
<span data-ttu-id="57722-117">Dies ist ein Array von Qubits, das eine ganze Zahl im Little-Endian-Format codiert.</span><span class="sxs-lookup"><span data-stu-id="57722-117">This is an array of qubits encoding an integer in little-endian format.</span></span>



## <a name="output--unit"></a><span data-ttu-id="57722-118">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="57722-118">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="57722-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="57722-119">Remarks</span></span>

- <span data-ttu-id="57722-120">Ein Leit Diagramm und eine Erläuterung finden Sie in Abbildung 7 auf [Seite 8 von arXiv: quant-ph/0205095v3](https://arxiv.org/pdf/quant-ph/0205095v3.pdf#page=8)</span><span class="sxs-lookup"><span data-stu-id="57722-120">For the circuit diagram and explanation see Figure 7 on [Page 8 of arXiv:quant-ph/0205095v3](https://arxiv.org/pdf/quant-ph/0205095v3.pdf#page=8)</span></span>
- <span data-ttu-id="57722-121">Dieser Vorgang entspricht u ₐ in [arXiv: quant-ph/0205095v3](https://arxiv.org/pdf/quant-ph/0205095v3.pdf)</span><span class="sxs-lookup"><span data-stu-id="57722-121">This operation corresponds to Uₐ in [arXiv:quant-ph/0205095v3](https://arxiv.org/pdf/quant-ph/0205095v3.pdf)</span></span>