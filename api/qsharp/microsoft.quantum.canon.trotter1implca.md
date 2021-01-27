---
uid: Microsoft.Quantum.Canon.Trotter1ImplCA
title: Trotter1ImplCA-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Trotter1ImplCA
qsharp.summary: Implementation of the first-order Trotter–Suzuki integrator.
ms.openlocfilehash: 6de4b6e7a34d66037d83a6e2bd5821402207c743
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840104"
---
# <a name="trotter1implca-operation"></a><span data-ttu-id="25a04-102">Trotter1ImplCA-Vorgang</span><span class="sxs-lookup"><span data-stu-id="25a04-102">Trotter1ImplCA operation</span></span>

<span data-ttu-id="25a04-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="25a04-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="25a04-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="25a04-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="25a04-105">Implementierung des Trotters der ersten Bestellung – Suzuki Integrator.</span><span class="sxs-lookup"><span data-stu-id="25a04-105">Implementation of the first-order Trotter–Suzuki integrator.</span></span>

```qsharp
operation Trotter1ImplCA<'T> ((nSteps : Int, op : ((Int, Double, 'T) => Unit is Adj + Ctl)), stepSize : Double, target : 'T) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="25a04-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="25a04-106">Input</span></span>

### <a name="nsteps--int"></a><span data-ttu-id="25a04-107">nsteps: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="25a04-107">nSteps : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="25a04-108">Die Anzahl der Vorgänge, die in Zeitschritten zerlegt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="25a04-108">The number of operations to be decomposed into time steps.</span></span>


### <a name="op--intdoublet--unit--is-adj--ctl"></a><span data-ttu-id="25a04-109">OP: ([int](xref:microsoft.quantum.lang-ref.int),[Double](xref:microsoft.quantum.lang-ref.double), 't) => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="25a04-109">op : ([Int](xref:microsoft.quantum.lang-ref.int),[Double](xref:microsoft.quantum.lang-ref.double),'T) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="25a04-110">Ein Vorgang, bei dem eine Index Eingabe (Type `Int` ) und eine Zeiteingabe (Typ) `Double` und ein Quantum-Register (Typ `'T` ) für die Zerlegung akzeptiert werden.</span><span class="sxs-lookup"><span data-stu-id="25a04-110">An operation which accepts an index input (type `Int`) and a time input (type `Double`) and a quantum register (type `'T`) for decomposition.</span></span>


### <a name="stepsize--double"></a><span data-ttu-id="25a04-111">stepSize: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="25a04-111">stepSize : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="25a04-112">Multiplikator für die Größe der einzelnen Schritte der Simulation.</span><span class="sxs-lookup"><span data-stu-id="25a04-112">Multiplier on size of each step of the simulation.</span></span>


### <a name="target--t"></a><span data-ttu-id="25a04-113">Ziel: 't</span><span class="sxs-lookup"><span data-stu-id="25a04-113">target : 'T</span></span>

<span data-ttu-id="25a04-114">Ein Quantum-Register, für das der Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="25a04-114">A quantum register on which the operations act.</span></span>



## <a name="output--unit"></a><span data-ttu-id="25a04-115">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="25a04-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="25a04-116">Typparameter</span><span class="sxs-lookup"><span data-stu-id="25a04-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="25a04-117">GIF</span><span class="sxs-lookup"><span data-stu-id="25a04-117">'T</span></span>

<span data-ttu-id="25a04-118">Der Typ, auf den jeder Zeit Schritt reagieren soll. in der Regel entweder `Qubit[]` oder `Qubit` .</span><span class="sxs-lookup"><span data-stu-id="25a04-118">The type which each time step should act upon; typically, either `Qubit[]` or `Qubit`.</span></span>

## <a name="example"></a><span data-ttu-id="25a04-119">Beispiel</span><span class="sxs-lookup"><span data-stu-id="25a04-119">Example</span></span>

<span data-ttu-id="25a04-120">Die folgenden sind gleichwertig:</span><span class="sxs-lookup"><span data-stu-id="25a04-120">The following are equivalent:</span></span>

```qsharp
op(0, deltaT, target);
op(1, deltaT, target);
```

<span data-ttu-id="25a04-121">and</span><span class="sxs-lookup"><span data-stu-id="25a04-121">and</span></span>

```qsharp
Trotter1ImplCA((2, op), deltaT, target);
```