---
uid: Microsoft.Quantum.Canon.TrotterArbitraryImplCA
title: Vorgang "trotterarbiaryimplca"
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: TrotterArbitraryImplCA
qsharp.summary: Recursive implementation of even-order Trotter–Suzuki integrator.
ms.openlocfilehash: bb93517a479ce344277bfe97d070e6630a8fccc0
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840098"
---
# <a name="trotterarbitraryimplca-operation"></a><span data-ttu-id="2a951-102">Vorgang "trotterarbiaryimplca"</span><span class="sxs-lookup"><span data-stu-id="2a951-102">TrotterArbitraryImplCA operation</span></span>

<span data-ttu-id="2a951-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="2a951-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="2a951-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="2a951-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="2a951-105">Rekursive Implementierung des Trotters der geraden Ordnung – Suzuki Integrator.</span><span class="sxs-lookup"><span data-stu-id="2a951-105">Recursive implementation of even-order Trotter–Suzuki integrator.</span></span>

```qsharp
operation TrotterArbitraryImplCA<'T> (order : Int, (nSteps : Int, op : ((Int, Double, 'T) => Unit is Adj + Ctl)), stepSize : Double, target : 'T) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="2a951-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2a951-106">Input</span></span>

### <a name="order--int"></a><span data-ttu-id="2a951-107">Reihenfolge: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="2a951-107">order : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="2a951-108">Reihenfolge von Trotter-Suzuki Integrator.</span><span class="sxs-lookup"><span data-stu-id="2a951-108">Order of Trotter-Suzuki integrator.</span></span>


### <a name="nsteps--int"></a><span data-ttu-id="2a951-109">nsteps: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="2a951-109">nSteps : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="2a951-110">Die Anzahl der Vorgänge, die in Zeitschritten zerlegt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="2a951-110">The number of operations to be decomposed into time steps.</span></span>


### <a name="op--intdoublet--unit--is-adj--ctl"></a><span data-ttu-id="2a951-111">OP: ([int](xref:microsoft.quantum.lang-ref.int),[Double](xref:microsoft.quantum.lang-ref.double), 't) => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="2a951-111">op : ([Int](xref:microsoft.quantum.lang-ref.int),[Double](xref:microsoft.quantum.lang-ref.double),'T) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="2a951-112">Ein Vorgang, bei dem eine Index Eingabe (Type `Int` ) und eine Zeiteingabe (Typ) `Double` und ein Quantum-Register (Typ `'T` ) für die Zerlegung akzeptiert werden.</span><span class="sxs-lookup"><span data-stu-id="2a951-112">An operation which accepts an index input (type `Int`) and a time input (type `Double`) and a quantum register (type `'T`) for decomposition.</span></span>


### <a name="stepsize--double"></a><span data-ttu-id="2a951-113">stepSize: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="2a951-113">stepSize : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="2a951-114">Multiplikator für die Größe der einzelnen Schritte der Simulation.</span><span class="sxs-lookup"><span data-stu-id="2a951-114">Multiplier on size of each step of the simulation.</span></span>


### <a name="target--t"></a><span data-ttu-id="2a951-115">Ziel: 't</span><span class="sxs-lookup"><span data-stu-id="2a951-115">target : 'T</span></span>

<span data-ttu-id="2a951-116">Ein Quantum-Register, für das der Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2a951-116">A quantum register on which the operations act.</span></span>



## <a name="output--unit"></a><span data-ttu-id="2a951-117">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="2a951-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="2a951-118">Typparameter</span><span class="sxs-lookup"><span data-stu-id="2a951-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="2a951-119">GIF</span><span class="sxs-lookup"><span data-stu-id="2a951-119">'T</span></span>

<span data-ttu-id="2a951-120">Der Typ, auf den jeder Zeit Schritt reagieren soll. in der Regel entweder `Qubit[]` oder `Qubit` .</span><span class="sxs-lookup"><span data-stu-id="2a951-120">The type which each time step should act upon; typically, either `Qubit[]` or `Qubit`.</span></span>