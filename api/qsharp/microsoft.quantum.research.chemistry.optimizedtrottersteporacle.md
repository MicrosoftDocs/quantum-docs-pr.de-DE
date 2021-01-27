---
uid: Microsoft.Quantum.Research.Chemistry.OptimizedTrotterStepOracle
title: Optimizedtrottersteporacle-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Research.Chemistry
qsharp.name: OptimizedTrotterStepOracle
qsharp.summary: Returns optimized Trotter step operation and the parameters necessary to run it.
ms.openlocfilehash: 523a31564ae5f054fd60161f9981c43d3467f3d9
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842291"
---
# <a name="optimizedtrottersteporacle-function"></a><span data-ttu-id="dd6f4-102">Optimizedtrottersteporacle-Funktion</span><span class="sxs-lookup"><span data-stu-id="dd6f4-102">OptimizedTrotterStepOracle function</span></span>

<span data-ttu-id="dd6f4-103">Namespace: [Microsoft. Quantum. Research. Chemistry](xref:Microsoft.Quantum.Research.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="dd6f4-103">Namespace: [Microsoft.Quantum.Research.Chemistry](xref:Microsoft.Quantum.Research.Chemistry)</span></span>

<span data-ttu-id="dd6f4-104">Paket: [Microsoft. Quantum. Research. Chemistry](https://nuget.org/packages/Microsoft.Quantum.Research.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="dd6f4-104">Package: [Microsoft.Quantum.Research.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Research.Chemistry)</span></span>


<span data-ttu-id="dd6f4-105">Gibt den optimierten Vorgang für den Schritt und die für die Ausführung erforderlichen Parameter zurück.</span><span class="sxs-lookup"><span data-stu-id="dd6f4-105">Returns optimized Trotter step operation and the parameters necessary to run it.</span></span>

```qsharp
function OptimizedTrotterStepOracle (qSharpData : Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerEncodingData, trotterStepSize : Double, trotterOrder : Int) : (Int, (Double, (Qubit[] => Unit is Adj + Ctl)))
```


## <a name="input"></a><span data-ttu-id="dd6f4-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="dd6f4-106">Input</span></span>

### <a name="qsharpdata--jordanwignerencodingdata"></a><span data-ttu-id="dd6f4-107">qsharpdata: [jordanwignerencodingdata](xref:Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerEncodingData)</span><span class="sxs-lookup"><span data-stu-id="dd6f4-107">qSharpData : [JordanWignerEncodingData](xref:Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerEncodingData)</span></span>

<span data-ttu-id="dd6f4-108">Hamiltona wird nach `JordanWignerEncodingData` Format beschrieben.</span><span class="sxs-lookup"><span data-stu-id="dd6f4-108">Hamiltonian described by `JordanWignerEncodingData` format.</span></span>


### <a name="trotterstepsize--double"></a><span data-ttu-id="dd6f4-109">trotterstepsize: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="dd6f4-109">trotterStepSize : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="dd6f4-110">Schrittgröße des trotterintegrator.</span><span class="sxs-lookup"><span data-stu-id="dd6f4-110">Step size of Trotter integrator.</span></span>


### <a name="trotterorder--int"></a><span data-ttu-id="dd6f4-111">trotterorder: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="dd6f4-111">trotterOrder : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="dd6f4-112">Reihenfolge des trockintegrator.</span><span class="sxs-lookup"><span data-stu-id="dd6f4-112">Order of Trotter integrator.</span></span>



## <a name="output--intdoublequbit--unit--is-adj--ctl"></a><span data-ttu-id="dd6f4-113">Ausgabe: ([int](xref:microsoft.quantum.lang-ref.int), ([Double](xref:microsoft.quantum.lang-ref.double),[Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL))</span><span class="sxs-lookup"><span data-stu-id="dd6f4-113">Output : ([Int](xref:microsoft.quantum.lang-ref.int),([Double](xref:microsoft.quantum.lang-ref.double),[Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl))</span></span>

<span data-ttu-id="dd6f4-114">Ein Tupel, wobei: `Int` die Anzahl der zugeordneten Qubits ist, `Double` `1.0/trotterStepSize` und der Vorgang ist der trockschritt.</span><span class="sxs-lookup"><span data-stu-id="dd6f4-114">A tuple where: `Int` is the number of qubits allocated, `Double` is `1.0/trotterStepSize`, and the operation is the Trotter step.</span></span>