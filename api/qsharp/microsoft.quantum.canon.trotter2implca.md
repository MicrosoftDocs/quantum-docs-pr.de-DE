---
uid: Microsoft.Quantum.Canon.Trotter2ImplCA
title: Trotter2ImplCA-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Trotter2ImplCA
qsharp.summary: Implementation of the second-order Trotter–Suzuki integrator.
ms.openlocfilehash: 34b60934b67c19b2d1d718d68b85a2f0fffeab5d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98852018"
---
# <a name="trotter2implca-operation"></a><span data-ttu-id="2eaaa-102">Trotter2ImplCA-Vorgang</span><span class="sxs-lookup"><span data-stu-id="2eaaa-102">Trotter2ImplCA operation</span></span>

<span data-ttu-id="2eaaa-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="2eaaa-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="2eaaa-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="2eaaa-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="2eaaa-105">Implementierung des Trotters der zweiten Ordnung – Suzuki Integrator.</span><span class="sxs-lookup"><span data-stu-id="2eaaa-105">Implementation of the second-order Trotter–Suzuki integrator.</span></span>

```qsharp
operation Trotter2ImplCA<'T> ((nSteps : Int, op : ((Int, Double, 'T) => Unit is Adj + Ctl)), stepSize : Double, target : 'T) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="2eaaa-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2eaaa-106">Input</span></span>

### <a name="nsteps--int"></a><span data-ttu-id="2eaaa-107">nsteps: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="2eaaa-107">nSteps : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="2eaaa-108">Die Anzahl der Vorgänge, die in Zeitschritten zerlegt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="2eaaa-108">The number of operations to be decomposed into time steps.</span></span>


### <a name="op--intdoublet--unit--is-adj--ctl"></a><span data-ttu-id="2eaaa-109">OP: ([int](xref:microsoft.quantum.lang-ref.int),[Double](xref:microsoft.quantum.lang-ref.double), 't) => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="2eaaa-109">op : ([Int](xref:microsoft.quantum.lang-ref.int),[Double](xref:microsoft.quantum.lang-ref.double),'T) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="2eaaa-110">Ein Vorgang, bei dem eine Index Eingabe (Type `Int` ) und eine Zeiteingabe (Typ) `Double` und ein Quantum-Register (Typ `'T` ) für die Zerlegung akzeptiert werden.</span><span class="sxs-lookup"><span data-stu-id="2eaaa-110">An operation which accepts an index input (type `Int`) and a time input (type `Double`) and a quantum register (type `'T`) for decomposition.</span></span>


### <a name="stepsize--double"></a><span data-ttu-id="2eaaa-111">stepSize: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="2eaaa-111">stepSize : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="2eaaa-112">Multiplikator für die Größe der einzelnen Schritte der Simulation.</span><span class="sxs-lookup"><span data-stu-id="2eaaa-112">Multiplier on size of each step of the simulation.</span></span>


### <a name="target--t"></a><span data-ttu-id="2eaaa-113">Ziel: 't</span><span class="sxs-lookup"><span data-stu-id="2eaaa-113">target : 'T</span></span>

<span data-ttu-id="2eaaa-114">Ein Quantum-Register, für das der Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2eaaa-114">A quantum register on which the operations act.</span></span>



## <a name="output--unit"></a><span data-ttu-id="2eaaa-115">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="2eaaa-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="2eaaa-116">Typparameter</span><span class="sxs-lookup"><span data-stu-id="2eaaa-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="2eaaa-117">GIF</span><span class="sxs-lookup"><span data-stu-id="2eaaa-117">'T</span></span>

<span data-ttu-id="2eaaa-118">Der Typ, auf den jeder Zeit Schritt reagieren soll. in der Regel entweder `Qubit[]` oder `Qubit` .</span><span class="sxs-lookup"><span data-stu-id="2eaaa-118">The type which each time step should act upon; typically, either `Qubit[]` or `Qubit`.</span></span>

## <a name="example"></a><span data-ttu-id="2eaaa-119">Beispiel</span><span class="sxs-lookup"><span data-stu-id="2eaaa-119">Example</span></span>

<span data-ttu-id="2eaaa-120">Die folgenden sind gleichwertig:</span><span class="sxs-lookup"><span data-stu-id="2eaaa-120">The following are equivalent:</span></span>

```qsharp
op(0, deltaT / 2.0, target);
op(1, deltaT / 2.0, target);
op(1, deltaT / 2.0, target);
op(0, deltaT / 2.0, target);
```

<span data-ttu-id="2eaaa-121">and</span><span class="sxs-lookup"><span data-stu-id="2eaaa-121">and</span></span>

```qsharp
Trotter2ImplCA((2, op), deltaT, target);
```