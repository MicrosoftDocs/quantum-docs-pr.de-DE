---
uid: Microsoft.Quantum.Preparation.PrepareUniformSuperposition
title: Prepareuniforsuperposition-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PrepareUniformSuperposition
qsharp.summary: >-
  Creates a uniform superposition over states that encode 0 through `nIndices - 1`.

  That is, this unitary $U$ creates a uniform superposition over all number states $0$ to $M-1$, given an input state $\ket{0\cdots 0}$. In other words, $$ \begin{align} U\ket{0}=\frac{1}{\sqrt{M}}\sum_{j=0}^{M-1}\ket{j}. \end{align} $$.
ms.openlocfilehash: 9b9f182ed7c1ea24ae74b8a2321a309042a17c97
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96230088"
---
# <a name="prepareuniformsuperposition-operation"></a><span data-ttu-id="cd06b-102">Prepareuniforsuperposition-Vorgang</span><span class="sxs-lookup"><span data-stu-id="cd06b-102">PrepareUniformSuperposition operation</span></span>

<span data-ttu-id="cd06b-103">Namespace: [Microsoft. Quantum. Preparation](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="cd06b-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="cd06b-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="cd06b-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="cd06b-105">Erstellt eine einheitliche Superposition über Zustände, die 0 bis codieren `nIndices - 1` .</span><span class="sxs-lookup"><span data-stu-id="cd06b-105">Creates a uniform superposition over states that encode 0 through `nIndices - 1`.</span></span>

<span data-ttu-id="cd06b-106">Das heißt, dieser einheitliche $U $ erstellt eine einheitliche Superposition für alle Zahl Zustände $0 $ bis $M-$1, wenn ein Eingabe Status $ \ket{0\cdots 0} $ angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="cd06b-106">That is, this unitary $U$ creates a uniform superposition over all number states $0$ to $M-1$, given an input state $\ket{0\cdots 0}$.</span></span> <span data-ttu-id="cd06b-107">Anders ausgedrückt: $ $ \begin{align} u\ket {0} = \frac {1} {\sqrt{m}}\ sum_ {j = 0} ^ {M-1} \ket{j}.</span><span class="sxs-lookup"><span data-stu-id="cd06b-107">In other words, $$ \begin{align} U\ket{0}=\frac{1}{\sqrt{M}}\sum_{j=0}^{M-1}\ket{j}.</span></span>
<span data-ttu-id="cd06b-108">\end{align} $ $.</span><span class="sxs-lookup"><span data-stu-id="cd06b-108">\end{align} $$.</span></span>

```qsharp
operation PrepareUniformSuperposition (nIndices : Int, indexRegister : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="cd06b-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="cd06b-109">Input</span></span>

### <a name="nindices--int"></a><span data-ttu-id="cd06b-110">nindizes: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="cd06b-110">nIndices : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="cd06b-111">Die gewünschte Anzahl von Zuständen $M $ in der einheitlichen Superposition.</span><span class="sxs-lookup"><span data-stu-id="cd06b-111">The desired number of states $M$ in the uniform superposition.</span></span>


### <a name="indexregister--littleendian"></a><span data-ttu-id="cd06b-112">Indexregister: [littleerdian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="cd06b-112">indexRegister : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="cd06b-113">Das Qubit-Register, das die Zahlen Zustände im- `LittleEndian` Format speichert.</span><span class="sxs-lookup"><span data-stu-id="cd06b-113">The qubit register that stores the number states in `LittleEndian` format.</span></span>
<span data-ttu-id="cd06b-114">Dieses Register muss in der Lage sein, die Zahl $M-$1 zu speichern, und es wird davon ausgegangen, dass es im Status $ \ket{0\cdots 0} $ initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="cd06b-114">This register must be able to store the number $M-1$, and is assumed to be initialized in the state $\ket{0\cdots 0}$.</span></span>



## <a name="output--unit"></a><span data-ttu-id="cd06b-115">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="cd06b-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="cd06b-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cd06b-116">Remarks</span></span>

<span data-ttu-id="cd06b-117">Der Vorgang ist "adjointable", erfordert jedoch, dass `indexRegister` sich in diesem Fall in einer einheitlichen übergeordneten Position befindet `nIndices` .</span><span class="sxs-lookup"><span data-stu-id="cd06b-117">The operation is adjointable, but requires that `indexRegister` is in a uniform superposition over the first `nIndices` basis states in that case.</span></span>