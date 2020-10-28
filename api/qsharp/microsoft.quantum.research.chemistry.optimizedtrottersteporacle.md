---
uid: Microsoft.Quantum.Research.Chemistry.OptimizedTrotterStepOracle
title: Optimizedtrottersteporacle-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Research.Chemistry
qsharp.name: OptimizedTrotterStepOracle
qsharp.summary: Returns optimized Trotter step operation and the parameters necessary to run it.
ms.openlocfilehash: f78d80f7ab71f4fc759d8045c9a134d7178aaa15
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92701802"
---
# <a name="optimizedtrottersteporacle-function"></a><span data-ttu-id="f02d6-102">Optimizedtrottersteporacle-Funktion</span><span class="sxs-lookup"><span data-stu-id="f02d6-102">OptimizedTrotterStepOracle function</span></span>

<span data-ttu-id="f02d6-103">Namespace: [Microsoft. Quantum. Research. Chemistry](xref:Microsoft.Quantum.Research.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="f02d6-103">Namespace: [Microsoft.Quantum.Research.Chemistry](xref:Microsoft.Quantum.Research.Chemistry)</span></span>

<span data-ttu-id="f02d6-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="f02d6-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="f02d6-105">Gibt den optimierten Vorgang für den Schritt und die für die Ausführung erforderlichen Parameter zurück.</span><span class="sxs-lookup"><span data-stu-id="f02d6-105">Returns optimized Trotter step operation and the parameters necessary to run it.</span></span>

```qsharp
function OptimizedTrotterStepOracle (qSharpData : Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerEncodingData, trotterStepSize : Double, trotterOrder : Int) : (Int, (Double, (Qubit[] => Unit is Adj + Ctl)))
```


## <a name="input"></a><span data-ttu-id="f02d6-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f02d6-106">Input</span></span>

### <a name="qsharpdata--jordanwignerencodingdata"></a><span data-ttu-id="f02d6-107">qsharpdata: [jordanwignerencodingdata](xref:Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerEncodingData)</span><span class="sxs-lookup"><span data-stu-id="f02d6-107">qSharpData : [JordanWignerEncodingData](xref:Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerEncodingData)</span></span>

<span data-ttu-id="f02d6-108">Hamiltona wird nach `JordanWignerEncodingData` Format beschrieben.</span><span class="sxs-lookup"><span data-stu-id="f02d6-108">Hamiltonian described by `JordanWignerEncodingData` format.</span></span>


### <a name="trotterstepsize--double"></a><span data-ttu-id="f02d6-109">trotterstepsize: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="f02d6-109">trotterStepSize : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="f02d6-110">Schrittgröße des trotterintegrator.</span><span class="sxs-lookup"><span data-stu-id="f02d6-110">Step size of Trotter integrator.</span></span>


### <a name="trotterorder--int"></a><span data-ttu-id="f02d6-111">trotterorder: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="f02d6-111">trotterOrder : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="f02d6-112">Reihenfolge des trockintegrator.</span><span class="sxs-lookup"><span data-stu-id="f02d6-112">Order of Trotter integrator.</span></span>



## <a name="output--intdoublequbit--unit-adj--ctl"></a><span data-ttu-id="f02d6-113">Ausgabe: ([int](xref:microsoft.quantum.lang-ref.int), ([Double](xref:microsoft.quantum.lang-ref.double),[Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL))</span><span class="sxs-lookup"><span data-stu-id="f02d6-113">Output : ([Int](xref:microsoft.quantum.lang-ref.int),([Double](xref:microsoft.quantum.lang-ref.double),[Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl))</span></span>

<span data-ttu-id="f02d6-114">Ein Tupel, wobei: `Int` die Anzahl der zugeordneten Qubits ist, `Double` `1.0/trotterStepSize` und der Vorgang ist der trockschritt.</span><span class="sxs-lookup"><span data-stu-id="f02d6-114">A tuple where: `Int` is the number of qubits allocated, `Double` is `1.0/trotterStepSize`, and the operation is the Trotter step.</span></span>