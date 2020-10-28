---
uid: Microsoft.Quantum.Canon.TrotterArbitraryImplCA
title: Vorgang "trotterarbiaryimplca"
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: TrotterArbitraryImplCA
qsharp.summary: Recursive implementation of even-order Trotter–Suzuki integrator.
ms.openlocfilehash: 1c094d09ac8bdd71a59ef57d8715a6f90f18efc6
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703746"
---
# <a name="trotterarbitraryimplca-operation"></a><span data-ttu-id="bf2cf-102">Vorgang "trotterarbiaryimplca"</span><span class="sxs-lookup"><span data-stu-id="bf2cf-102">TrotterArbitraryImplCA operation</span></span>

<span data-ttu-id="bf2cf-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="bf2cf-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="bf2cf-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="bf2cf-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="bf2cf-105">Rekursive Implementierung des Trotters der geraden Ordnung – Suzuki Integrator.</span><span class="sxs-lookup"><span data-stu-id="bf2cf-105">Recursive implementation of even-order Trotter–Suzuki integrator.</span></span>

```qsharp
operation TrotterArbitraryImplCA<'T> (order : Int, (nSteps : Int, op : ((Int, Double, 'T) => Unit is Adj + Ctl)), stepSize : Double, target : 'T) : Unit
```


## <a name="input"></a><span data-ttu-id="bf2cf-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="bf2cf-106">Input</span></span>

### <a name="order--int"></a><span data-ttu-id="bf2cf-107">Reihenfolge: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="bf2cf-107">order : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="bf2cf-108">Reihenfolge von Trotter-Suzuki Integrator.</span><span class="sxs-lookup"><span data-stu-id="bf2cf-108">Order of Trotter-Suzuki integrator.</span></span>


### <a name="nsteps--int"></a><span data-ttu-id="bf2cf-109">nsteps: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="bf2cf-109">nSteps : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="bf2cf-110">Die Anzahl der Vorgänge, die in Zeitschritten zerlegt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="bf2cf-110">The number of operations to be decomposed into time steps.</span></span>


### <a name="op--intdoublet--unit-adj--ctl"></a><span data-ttu-id="bf2cf-111">OP: ([int](xref:microsoft.quantum.lang-ref.int),[Double](xref:microsoft.quantum.lang-ref.double), t) => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="bf2cf-111">op : ([Int](xref:microsoft.quantum.lang-ref.int),[Double](xref:microsoft.quantum.lang-ref.double),'T) => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="bf2cf-112">Ein Vorgang, bei dem eine Index Eingabe (Type `Int` ) und eine Zeiteingabe (Typ) `Double` und ein Quantum-Register (Typ `'T` ) für die Zerlegung akzeptiert werden.</span><span class="sxs-lookup"><span data-stu-id="bf2cf-112">An operation which accepts an index input (type `Int`) and a time input (type `Double`) and a quantum register (type `'T`) for decomposition.</span></span>


### <a name="stepsize--double"></a><span data-ttu-id="bf2cf-113">stepSize: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="bf2cf-113">stepSize : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="bf2cf-114">Multiplikator für die Größe der einzelnen Schritte der Simulation.</span><span class="sxs-lookup"><span data-stu-id="bf2cf-114">Multiplier on size of each step of the simulation.</span></span>


### <a name="target--t"></a><span data-ttu-id="bf2cf-115">Ziel: 't</span><span class="sxs-lookup"><span data-stu-id="bf2cf-115">target : 'T</span></span>

<span data-ttu-id="bf2cf-116">Ein Quantum-Register, für das der Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bf2cf-116">A quantum register on which the operations act.</span></span>



## <a name="output--unit"></a><span data-ttu-id="bf2cf-117">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="bf2cf-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="bf2cf-118">Typparameter</span><span class="sxs-lookup"><span data-stu-id="bf2cf-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="bf2cf-119">GIF</span><span class="sxs-lookup"><span data-stu-id="bf2cf-119">'T</span></span>

<span data-ttu-id="bf2cf-120">Der Typ, auf den jeder Zeit Schritt reagieren soll. in der Regel entweder `Qubit[]` oder `Qubit` .</span><span class="sxs-lookup"><span data-stu-id="bf2cf-120">The type which each time step should act upon; typically, either `Qubit[]` or `Qubit`.</span></span>