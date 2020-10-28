---
uid: Microsoft.Quantum.Canon.DecomposedIntoTimeStepsCA
title: Debug-Funktion (Funktion)
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: DecomposedIntoTimeStepsCA
qsharp.summary: Returns an operation implementing the Trotter–Suzuki integrator for a given operation.
ms.openlocfilehash: cfd563c1c6350255364de1e227442624acc98c22
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704266"
---
# <a name="decomposedintotimestepsca-function"></a><span data-ttu-id="f5f86-102">Debug-Funktion (Funktion)</span><span class="sxs-lookup"><span data-stu-id="f5f86-102">DecomposedIntoTimeStepsCA function</span></span>

<span data-ttu-id="f5f86-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="f5f86-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="f5f86-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="f5f86-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="f5f86-105">Gibt einen Vorgang zurück, der den Trotter – Suzuki Integrator für einen angegebenen Vorgang implementiert.</span><span class="sxs-lookup"><span data-stu-id="f5f86-105">Returns an operation implementing the Trotter–Suzuki integrator for a given operation.</span></span>

```qsharp
function DecomposedIntoTimeStepsCA<'T> ((nSteps : Int, op : ((Int, Double, 'T) => Unit is Adj + Ctl)), trotterOrder : Int) : ((Double, 'T) => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="f5f86-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f5f86-106">Input</span></span>

### <a name="nsteps--int"></a><span data-ttu-id="f5f86-107">nsteps: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="f5f86-107">nSteps : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="f5f86-108">Die Anzahl der Vorgänge, die in Zeitschritten zerlegt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f5f86-108">The number of operations to be decomposed into time steps.</span></span>


### <a name="op--intdoublet--unit-adj--ctl"></a><span data-ttu-id="f5f86-109">OP: ([int](xref:microsoft.quantum.lang-ref.int),[Double](xref:microsoft.quantum.lang-ref.double), t) => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="f5f86-109">op : ([Int](xref:microsoft.quantum.lang-ref.int),[Double](xref:microsoft.quantum.lang-ref.double),'T) => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="f5f86-110">Ein Vorgang, bei dem eine Index Eingabe (Type `Int` ) und eine Zeiteingabe (Typ `Double` ) für die Zerlegung akzeptiert werden.</span><span class="sxs-lookup"><span data-stu-id="f5f86-110">An operation which accepts an index input (type `Int`) and a time input (type `Double`) for decomposition.</span></span>


### <a name="trotterorder--int"></a><span data-ttu-id="f5f86-111">trotterorder: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="f5f86-111">trotterOrder : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="f5f86-112">Wählt die Reihenfolge des zu verwendenden Trotter – Suzuki Integrator aus.</span><span class="sxs-lookup"><span data-stu-id="f5f86-112">Selects the order of the Trotter–Suzuki integrator to be used.</span></span>
<span data-ttu-id="f5f86-113">Bestellung 1 und sogar Orders 2, 4, 6,... werden zurzeit unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f5f86-113">Order 1 and even orders 2, 4, 6,... are currently supported.</span></span>



## <a name="output--doublet--unit-adj--ctl"></a><span data-ttu-id="f5f86-114">Ausgabe: ([Double](xref:microsoft.quantum.lang-ref.double), t) => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="f5f86-114">Output : ([Double](xref:microsoft.quantum.lang-ref.double),'T) => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="f5f86-115">Gibt eine einheitliche-Klasse zurück, die den Trotter – Suzuki Integrator implementiert, wobei der erste Parameter `Double` die Größe des Integrations Schritts ist und der zweite Parameter das Ziel ist.</span><span class="sxs-lookup"><span data-stu-id="f5f86-115">Returns a unitary implementing the Trotter–Suzuki integrator, where the first parameter `Double` is the integration step size, and the second parameter is the target acted upon.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="f5f86-116">Typparameter</span><span class="sxs-lookup"><span data-stu-id="f5f86-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="f5f86-117">GIF</span><span class="sxs-lookup"><span data-stu-id="f5f86-117">'T</span></span>

<span data-ttu-id="f5f86-118">Der Typ, auf den jeder Zeit Schritt reagieren soll. in der Regel entweder `Qubit[]` oder `Qubit` .</span><span class="sxs-lookup"><span data-stu-id="f5f86-118">The type which each time step should act upon; typically, either `Qubit[]` or `Qubit`.</span></span>

## <a name="remarks"></a><span data-ttu-id="f5f86-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f5f86-119">Remarks</span></span>

<span data-ttu-id="f5f86-120">Wenn `order` Diese Funktion mit gleich `1` ist, gibt diese Funktion einen Vorgang zurück, der durch die niedrigste Reihenfolge (Trotter – Suzuki Integrator $ $ \begin{align} S_1 (\lambda) = \ prod_ {j = 1} ^ {m} e ^ {H_j \lambda}) simuliert werden kann. \end{align} $ $, wobei die Notation von [quant-ph/0508139](https://arxiv.org/abs/quant-ph/0508139) befolgt wurde und $ \lambda $ die Entwicklungszeit (dargestellt durch die erste Eingabe der zurückgegebenen Operation) ist. und lassen Sie $ \{ H_j \} _ {j = 1} ^ {m} $ den Satz der (Schiefe-hermitian) Dynamical-Generatoren aufweisen, die integriert werden, sodass `op(j, lambda, _)` vom einheitlichen Operator $e ^ {H_j \lambda} $ simuliert wird.</span><span class="sxs-lookup"><span data-stu-id="f5f86-120">When called with `order` equal to `1`, this function returns an operation that can be simulated by the lowest-order Trotter–Suzuki integrator $$ \begin{align} S_1(\lambda) = \prod_{j = 1}^{m} e^{H_j \lambda}, \end{align} $$ where we have followed the notation of [quant-ph/0508139](https://arxiv.org/abs/quant-ph/0508139) and let $\lambda$ be the evolution time (represented by the first input of the returned operation), and have let $\{H_j\}_{j = 1}^{m}$ be the set of (skew-Hermitian) dynamical generators being integrated such that `op(j, lambda, _)` is simulated by the unitary operator $e^{H_j \lambda}$.</span></span>

<span data-ttu-id="f5f86-121">Ebenso gibt ein `order` von `2` den symmetrischen Trotter der zweiten Ordnung zurück – Suzuki Integrator $ $ \begin{align} S_2 (\lambda) = \ prod_ {j = 1} ^ {m} e ^ {H_k \lambda/2} \ prod_ {j ' = m} ^ {1} e ^ {H_ {j '} \lambda/2}.</span><span class="sxs-lookup"><span data-stu-id="f5f86-121">Similarly, an `order` of `2` returns the second-order symmetric Trotter–Suzuki integrator $$ \begin{align} S_2(\lambda) = \prod_{j = 1}^{m} e^{H_k \lambda / 2} \prod_{j' = m}^{1} e^{H_{j'} \lambda / 2}.</span></span>
<span data-ttu-id="f5f86-122">\end{align} $ $</span><span class="sxs-lookup"><span data-stu-id="f5f86-122">\end{align} $$</span></span>

<span data-ttu-id="f5f86-123">Höhere gerade Werte von `order` werden mithilfe der rekursiven Konstruktion von [quant-ph/0508139](https://arxiv.org/abs/quant-ph/0508139)implementiert.</span><span class="sxs-lookup"><span data-stu-id="f5f86-123">Higher even values of `order` are implemented using the recursive construction of [quant-ph/0508139](https://arxiv.org/abs/quant-ph/0508139).</span></span>

## <a name="references"></a><span data-ttu-id="f5f86-124">Referenzen</span><span class="sxs-lookup"><span data-stu-id="f5f86-124">References</span></span>

- [<span data-ttu-id="f5f86-125">*D. W. Beeren, G. ahukas, R. Cleve, B. C. Sanders*</span><span class="sxs-lookup"><span data-stu-id="f5f86-125"> *D. W. Berry, G. Ahokas, R. Cleve, B. C. Sanders* </span></span>](https://arxiv.org/abs/quant-ph/0508139)