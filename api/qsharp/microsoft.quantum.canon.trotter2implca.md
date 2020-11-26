---
uid: Microsoft.Quantum.Canon.Trotter2ImplCA
title: Trotter2ImplCA-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Trotter2ImplCA
qsharp.summary: Implementation of the second-order Trotter–Suzuki integrator.
ms.openlocfilehash: 0e3a7e53a4d415e6b5af81d9bb3f52cddf36c4b3
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96204741"
---
# <a name="trotter2implca-operation"></a><span data-ttu-id="41627-102">Trotter2ImplCA-Vorgang</span><span class="sxs-lookup"><span data-stu-id="41627-102">Trotter2ImplCA operation</span></span>

<span data-ttu-id="41627-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="41627-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="41627-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="41627-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="41627-105">Implementierung des Trotters der zweiten Ordnung – Suzuki Integrator.</span><span class="sxs-lookup"><span data-stu-id="41627-105">Implementation of the second-order Trotter–Suzuki integrator.</span></span>

```qsharp
operation Trotter2ImplCA<'T> ((nSteps : Int, op : ((Int, Double, 'T) => Unit is Adj + Ctl)), stepSize : Double, target : 'T) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="41627-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="41627-106">Input</span></span>

### <a name="nsteps--int"></a><span data-ttu-id="41627-107">nsteps: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="41627-107">nSteps : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="41627-108">Die Anzahl der Vorgänge, die in Zeitschritten zerlegt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="41627-108">The number of operations to be decomposed into time steps.</span></span>


### <a name="op--intdoublet--unit--is-adj--ctl"></a><span data-ttu-id="41627-109">OP: ([int](xref:microsoft.quantum.lang-ref.int),[Double](xref:microsoft.quantum.lang-ref.double), 't) => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="41627-109">op : ([Int](xref:microsoft.quantum.lang-ref.int),[Double](xref:microsoft.quantum.lang-ref.double),'T) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="41627-110">Ein Vorgang, bei dem eine Index Eingabe (Type `Int` ) und eine Zeiteingabe (Typ) `Double` und ein Quantum-Register (Typ `'T` ) für die Zerlegung akzeptiert werden.</span><span class="sxs-lookup"><span data-stu-id="41627-110">An operation which accepts an index input (type `Int`) and a time input (type `Double`) and a quantum register (type `'T`) for decomposition.</span></span>


### <a name="stepsize--double"></a><span data-ttu-id="41627-111">stepSize: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="41627-111">stepSize : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="41627-112">Multiplikator für die Größe der einzelnen Schritte der Simulation.</span><span class="sxs-lookup"><span data-stu-id="41627-112">Multiplier on size of each step of the simulation.</span></span>


### <a name="target--t"></a><span data-ttu-id="41627-113">Ziel: 't</span><span class="sxs-lookup"><span data-stu-id="41627-113">target : 'T</span></span>

<span data-ttu-id="41627-114">Ein Quantum-Register, für das der Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="41627-114">A quantum register on which the operations act.</span></span>



## <a name="output--unit"></a><span data-ttu-id="41627-115">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="41627-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="41627-116">Typparameter</span><span class="sxs-lookup"><span data-stu-id="41627-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="41627-117">GIF</span><span class="sxs-lookup"><span data-stu-id="41627-117">'T</span></span>

<span data-ttu-id="41627-118">Der Typ, auf den jeder Zeit Schritt reagieren soll. in der Regel entweder `Qubit[]` oder `Qubit` .</span><span class="sxs-lookup"><span data-stu-id="41627-118">The type which each time step should act upon; typically, either `Qubit[]` or `Qubit`.</span></span>