---
uid: Microsoft.Quantum.Preparation.PrepareUniformSuperposition
title: Prepareuniforsuperposition-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PrepareUniformSuperposition
qsharp.summary: >-
  Creates a uniform superposition over states that encode 0 through `nIndices - 1`.

  That is, this unitary $U$ creates a uniform superposition over all number states $0$ to $M-1$, given an input state $\ket{0\cdots 0}$. In other words, $$ \begin{align} U\ket{0}=\frac{1}{\sqrt{M}}\sum_{j=0}^{M-1}\ket{j}. \end{align} $$.
ms.openlocfilehash: dc9d4ce1638b397748cafaa757241ce78633c67c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854321"
---
# <a name="prepareuniformsuperposition-operation"></a><span data-ttu-id="69d10-102">Prepareuniforsuperposition-Vorgang</span><span class="sxs-lookup"><span data-stu-id="69d10-102">PrepareUniformSuperposition operation</span></span>

<span data-ttu-id="69d10-103">Namespace: [Microsoft. Quantum. Preparation](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="69d10-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="69d10-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="69d10-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="69d10-105">Erstellt eine einheitliche Superposition über Zustände, die 0 bis codieren `nIndices - 1` .</span><span class="sxs-lookup"><span data-stu-id="69d10-105">Creates a uniform superposition over states that encode 0 through `nIndices - 1`.</span></span>

<span data-ttu-id="69d10-106">Das heißt, dieser einheitliche $U $ erstellt eine einheitliche Superposition für alle Zahl Zustände $0 $ bis $M-$1, wenn ein Eingabe Status $ \ket{0\cdots 0} $ angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="69d10-106">That is, this unitary $U$ creates a uniform superposition over all number states $0$ to $M-1$, given an input state $\ket{0\cdots 0}$.</span></span> <span data-ttu-id="69d10-107">Anders ausgedrückt: $ $ \begin{align} u\ket {0} = \frac {1} {\sqrt{m}}\ sum_ {j = 0} ^ {M-1} \ket{j}.</span><span class="sxs-lookup"><span data-stu-id="69d10-107">In other words, $$ \begin{align} U\ket{0}=\frac{1}{\sqrt{M}}\sum_{j=0}^{M-1}\ket{j}.</span></span>
<span data-ttu-id="69d10-108">\end{align} $ $.</span><span class="sxs-lookup"><span data-stu-id="69d10-108">\end{align} $$.</span></span>

```qsharp
operation PrepareUniformSuperposition (nIndices : Int, indexRegister : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="69d10-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="69d10-109">Input</span></span>

### <a name="nindices--int"></a><span data-ttu-id="69d10-110">nindizes: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="69d10-110">nIndices : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="69d10-111">Die gewünschte Anzahl von Zuständen $M $ in der einheitlichen Superposition.</span><span class="sxs-lookup"><span data-stu-id="69d10-111">The desired number of states $M$ in the uniform superposition.</span></span>


### <a name="indexregister--littleendian"></a><span data-ttu-id="69d10-112">Indexregister: [littleerdian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="69d10-112">indexRegister : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="69d10-113">Das Qubit-Register, das die Zahlen Zustände im- `LittleEndian` Format speichert.</span><span class="sxs-lookup"><span data-stu-id="69d10-113">The qubit register that stores the number states in `LittleEndian` format.</span></span>
<span data-ttu-id="69d10-114">Dieses Register muss in der Lage sein, die Zahl $M-$1 zu speichern, und es wird davon ausgegangen, dass es im Status $ \ket{0\cdots 0} $ initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="69d10-114">This register must be able to store the number $M-1$, and is assumed to be initialized in the state $\ket{0\cdots 0}$.</span></span>



## <a name="output--unit"></a><span data-ttu-id="69d10-115">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="69d10-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="example"></a><span data-ttu-id="69d10-116">Beispiel</span><span class="sxs-lookup"><span data-stu-id="69d10-116">Example</span></span>

<span data-ttu-id="69d10-117">Im folgenden Beispiel wird der Status $ \frac {1} {\sqrt {6} } \ sum_ {j = 0} ^ {5} \ket{j} $ auf $3 $ Qubits vorbereitet.</span><span class="sxs-lookup"><span data-stu-id="69d10-117">The following example prepares the state $\frac{1}{\sqrt{6}}\sum_{j=0}^{5}\ket{j}$ on $3$ qubits.</span></span>

```qsharp
let nIndices = 6;
using(indexRegister = Qubit[3]) {
    PrepareUniformSuperposition(nIndices, LittleEndian(indexRegister));
    // ...
}
```

## <a name="remarks"></a><span data-ttu-id="69d10-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="69d10-118">Remarks</span></span>

<span data-ttu-id="69d10-119">Der Vorgang ist "adjointable", erfordert jedoch, dass `indexRegister` sich in diesem Fall in einer einheitlichen übergeordneten Position befindet `nIndices` .</span><span class="sxs-lookup"><span data-stu-id="69d10-119">The operation is adjointable, but requires that `indexRegister` is in a uniform superposition over the first `nIndices` basis states in that case.</span></span>