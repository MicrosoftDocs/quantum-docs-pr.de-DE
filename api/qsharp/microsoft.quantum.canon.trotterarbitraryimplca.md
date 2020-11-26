---
uid: Microsoft.Quantum.Canon.TrotterArbitraryImplCA
title: Vorgang "trotterarbiaryimplca"
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: TrotterArbitraryImplCA
qsharp.summary: Recursive implementation of even-order Trotter–Suzuki integrator.
ms.openlocfilehash: 2abfbb9d51a98d8ede1b0835875a3771ffda0691
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96204724"
---
# <a name="trotterarbitraryimplca-operation"></a><span data-ttu-id="e622c-102">Vorgang "trotterarbiaryimplca"</span><span class="sxs-lookup"><span data-stu-id="e622c-102">TrotterArbitraryImplCA operation</span></span>

<span data-ttu-id="e622c-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="e622c-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="e622c-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="e622c-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="e622c-105">Rekursive Implementierung des Trotters der geraden Ordnung – Suzuki Integrator.</span><span class="sxs-lookup"><span data-stu-id="e622c-105">Recursive implementation of even-order Trotter–Suzuki integrator.</span></span>

```qsharp
operation TrotterArbitraryImplCA<'T> (order : Int, (nSteps : Int, op : ((Int, Double, 'T) => Unit is Adj + Ctl)), stepSize : Double, target : 'T) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="e622c-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e622c-106">Input</span></span>

### <a name="order--int"></a><span data-ttu-id="e622c-107">Reihenfolge: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="e622c-107">order : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="e622c-108">Reihenfolge von Trotter-Suzuki Integrator.</span><span class="sxs-lookup"><span data-stu-id="e622c-108">Order of Trotter-Suzuki integrator.</span></span>


### <a name="nsteps--int"></a><span data-ttu-id="e622c-109">nsteps: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="e622c-109">nSteps : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="e622c-110">Die Anzahl der Vorgänge, die in Zeitschritten zerlegt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e622c-110">The number of operations to be decomposed into time steps.</span></span>


### <a name="op--intdoublet--unit--is-adj--ctl"></a><span data-ttu-id="e622c-111">OP: ([int](xref:microsoft.quantum.lang-ref.int),[Double](xref:microsoft.quantum.lang-ref.double), 't) => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="e622c-111">op : ([Int](xref:microsoft.quantum.lang-ref.int),[Double](xref:microsoft.quantum.lang-ref.double),'T) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="e622c-112">Ein Vorgang, bei dem eine Index Eingabe (Type `Int` ) und eine Zeiteingabe (Typ) `Double` und ein Quantum-Register (Typ `'T` ) für die Zerlegung akzeptiert werden.</span><span class="sxs-lookup"><span data-stu-id="e622c-112">An operation which accepts an index input (type `Int`) and a time input (type `Double`) and a quantum register (type `'T`) for decomposition.</span></span>


### <a name="stepsize--double"></a><span data-ttu-id="e622c-113">stepSize: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="e622c-113">stepSize : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="e622c-114">Multiplikator für die Größe der einzelnen Schritte der Simulation.</span><span class="sxs-lookup"><span data-stu-id="e622c-114">Multiplier on size of each step of the simulation.</span></span>


### <a name="target--t"></a><span data-ttu-id="e622c-115">Ziel: 't</span><span class="sxs-lookup"><span data-stu-id="e622c-115">target : 'T</span></span>

<span data-ttu-id="e622c-116">Ein Quantum-Register, für das der Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e622c-116">A quantum register on which the operations act.</span></span>



## <a name="output--unit"></a><span data-ttu-id="e622c-117">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="e622c-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="e622c-118">Typparameter</span><span class="sxs-lookup"><span data-stu-id="e622c-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="e622c-119">GIF</span><span class="sxs-lookup"><span data-stu-id="e622c-119">'T</span></span>

<span data-ttu-id="e622c-120">Der Typ, auf den jeder Zeit Schritt reagieren soll. in der Regel entweder `Qubit[]` oder `Qubit` .</span><span class="sxs-lookup"><span data-stu-id="e622c-120">The type which each time step should act upon; typically, either `Qubit[]` or `Qubit`.</span></span>