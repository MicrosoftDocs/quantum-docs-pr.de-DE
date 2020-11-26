---
uid: Microsoft.Quantum.Arithmetic.IncrementByModularInteger
title: Incrementbymodularinteger-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: IncrementByModularInteger
qsharp.summary: Performs a modular increment of a qubit register by an integer constant.
ms.openlocfilehash: 8a02d22facce8f58180752b6d063ac55d75ca537
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96222948"
---
# <a name="incrementbymodularinteger-operation"></a><span data-ttu-id="57942-102">Incrementbymodularinteger-Vorgang</span><span class="sxs-lookup"><span data-stu-id="57942-102">IncrementByModularInteger operation</span></span>

<span data-ttu-id="57942-103">Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="57942-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="57942-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="57942-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="57942-105">Führt ein modulares Inkrement für ein Qubit-Register durch eine ganzzahlige Konstante aus.</span><span class="sxs-lookup"><span data-stu-id="57942-105">Performs a modular increment of a qubit register by an integer constant.</span></span>

```qsharp
operation IncrementByModularInteger (increment : Int, modulus : Int, target : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="57942-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="57942-106">Description</span></span>

<span data-ttu-id="57942-107">Geben Sie `increment` $a $ an, indem Sie `modulus` $N $ und Integer in `target` durch $y $ codiert haben.</span><span class="sxs-lookup"><span data-stu-id="57942-107">Let us denote `increment` by $a$, `modulus` by $N$ and integer encoded in `target` by $y$.</span></span>
<span data-ttu-id="57942-108">Anschließend führt der Vorgang die folgende Transformation aus: \begin{align} \ket{y} \mapsto \ket{(y + a) \operatschmue{mod} N} \end{align} ganze Zahlen werden im Little-Endian-Format codiert.</span><span class="sxs-lookup"><span data-stu-id="57942-108">Then the operation performs the following transformation: \begin{align} \ket{y} \mapsto \ket{(y + a) \operatorname{mod} N} \end{align} Integers are encoded in little-endian format.</span></span>

## <a name="input"></a><span data-ttu-id="57942-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="57942-109">Input</span></span>

### <a name="increment--int"></a><span data-ttu-id="57942-110">Inkrement: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="57942-110">increment : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="57942-111">Ganzzahliges Inkrement $a $, das $y $ hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="57942-111">Integer increment $a$ to be added to $y$.</span></span>


### <a name="modulus--int"></a><span data-ttu-id="57942-112">Modulo: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="57942-112">modulus : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="57942-113">Ganzzahliger $N $, $y + a $.</span><span class="sxs-lookup"><span data-stu-id="57942-113">Integer $N$ that mods $y + a$.</span></span>


### <a name="target--littleendian"></a><span data-ttu-id="57942-114">Ziel: [littleenddian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="57942-114">target : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="57942-115">Ganzzahliger $y $ im `LittleEndian` Format, dem `increment` $a $ hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="57942-115">Integer $y$ in `LittleEndian` format that `increment` $a$ is added to.</span></span>



## <a name="output--unit"></a><span data-ttu-id="57942-116">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="57942-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="57942-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="57942-117">Remarks</span></span>

<span data-ttu-id="57942-118">Geht davon aus, dass der Anfangswert von Target kleiner als $N $ und die Inkrement-$a $ kleiner als $N $ ist.</span><span class="sxs-lookup"><span data-stu-id="57942-118">Assumes that the initial value of target is less than $N$ and that the increment $a$ is less than $N$.</span></span>
<span data-ttu-id="57942-119">Beachten Sie, dass <xref:microsoft.quantum.arithmetic.incrementphasebymodularinteger> denselben Vorgang in der `PhaseLittleEndian` Basis implementiert.</span><span class="sxs-lookup"><span data-stu-id="57942-119">Note that <xref:microsoft.quantum.arithmetic.incrementphasebymodularinteger> implements the same operation in the `PhaseLittleEndian` basis.</span></span>

## <a name="see-also"></a><span data-ttu-id="57942-120">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="57942-120">See Also</span></span>

- [<span data-ttu-id="57942-121">Microsoft. Quantum. Arithmetik. incrementphasebymodularinteger</span><span class="sxs-lookup"><span data-stu-id="57942-121">Microsoft.Quantum.Arithmetic.IncrementPhaseByModularInteger</span></span>](xref:Microsoft.Quantum.Arithmetic.IncrementPhaseByModularInteger)