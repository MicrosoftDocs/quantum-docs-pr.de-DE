---
uid: Microsoft.Quantum.Arithmetic.IncrementByModularInteger
title: Incrementbymodularinteger-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: IncrementByModularInteger
qsharp.summary: Performs a modular increment of a qubit register by an integer constant.
ms.openlocfilehash: 271033b32b0de6cf600dca82126dab19c2bb4f5d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707263"
---
# <a name="incrementbymodularinteger-operation"></a><span data-ttu-id="2c094-102">Incrementbymodularinteger-Vorgang</span><span class="sxs-lookup"><span data-stu-id="2c094-102">IncrementByModularInteger operation</span></span>

<span data-ttu-id="2c094-103">Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="2c094-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="2c094-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="2c094-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="2c094-105">Führt ein modulares Inkrement für ein Qubit-Register durch eine ganzzahlige Konstante aus.</span><span class="sxs-lookup"><span data-stu-id="2c094-105">Performs a modular increment of a qubit register by an integer constant.</span></span>

```qsharp
operation IncrementByModularInteger (increment : Int, modulus : Int, target : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="description"></a><span data-ttu-id="2c094-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2c094-106">Description</span></span>

<span data-ttu-id="2c094-107">Geben Sie `increment` $a $ an, indem Sie `modulus` $N $ und Integer in `target` durch $y $ codiert haben.</span><span class="sxs-lookup"><span data-stu-id="2c094-107">Let us denote `increment` by $a$, `modulus` by $N$ and integer encoded in `target` by $y$.</span></span>
<span data-ttu-id="2c094-108">Anschließend führt der Vorgang die folgende Transformation aus: \begin{align} \ket{y} \mapsto \ket{(y + a) \operatschmue{mod} N} \end{align} ganze Zahlen werden im Little-Endian-Format codiert.</span><span class="sxs-lookup"><span data-stu-id="2c094-108">Then the operation performs the following transformation: \begin{align} \ket{y} \mapsto \ket{(y + a) \operatorname{mod} N} \end{align} Integers are encoded in little-endian format.</span></span>

## <a name="input"></a><span data-ttu-id="2c094-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2c094-109">Input</span></span>

### <a name="increment--int"></a><span data-ttu-id="2c094-110">Inkrement: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="2c094-110">increment : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="2c094-111">Ganzzahliges Inkrement $a $, das $y $ hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="2c094-111">Integer increment $a$ to be added to $y$.</span></span>


### <a name="modulus--int"></a><span data-ttu-id="2c094-112">Modulo: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="2c094-112">modulus : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="2c094-113">Ganzzahliger $N $, $y + a $.</span><span class="sxs-lookup"><span data-stu-id="2c094-113">Integer $N$ that mods $y + a$.</span></span>


### <a name="target--littleendian"></a><span data-ttu-id="2c094-114">Ziel: [littleenddian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="2c094-114">target : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="2c094-115">Ganzzahliger $y $ im `LittleEndian` Format, dem `increment` $a $ hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="2c094-115">Integer $y$ in `LittleEndian` format that `increment` $a$ is added to.</span></span>



## <a name="output--unit"></a><span data-ttu-id="2c094-116">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="2c094-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="2c094-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2c094-117">Remarks</span></span>

<span data-ttu-id="2c094-118">Geht davon aus, dass der Anfangswert von Target kleiner als $N $ und die Inkrement-$a $ kleiner als $N $ ist.</span><span class="sxs-lookup"><span data-stu-id="2c094-118">Assumes that the initial value of target is less than $N$ and that the increment $a$ is less than $N$.</span></span>
<span data-ttu-id="2c094-119">Beachten Sie, dass <xref:microsoft.quantum.arithmetic.incrementphasebymodularinteger> denselben Vorgang in der `PhaseLittleEndian` Basis implementiert.</span><span class="sxs-lookup"><span data-stu-id="2c094-119">Note that <xref:microsoft.quantum.arithmetic.incrementphasebymodularinteger> implements the same operation in the `PhaseLittleEndian` basis.</span></span>

## <a name="see-also"></a><span data-ttu-id="2c094-120">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="2c094-120">See Also</span></span>

- [<span data-ttu-id="2c094-121">Microsoft. Quantum. Arithmetik. incrementphasebymodularinteger</span><span class="sxs-lookup"><span data-stu-id="2c094-121">Microsoft.Quantum.Arithmetic.IncrementPhaseByModularInteger</span></span>](xref:Microsoft.Quantum.Arithmetic.IncrementPhaseByModularInteger)