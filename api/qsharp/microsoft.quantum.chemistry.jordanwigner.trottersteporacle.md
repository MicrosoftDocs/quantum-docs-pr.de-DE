---
uid: Microsoft.Quantum.Chemistry.JordanWigner.TrotterStepOracle
title: Trottersteporacle-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: TrotterStepOracle
qsharp.summary: Returns Trotter step operation and the parameters necessary to run it.
ms.openlocfilehash: a3164da1ce9ae1f72ec2fb1fa151159768cd5a4a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98835803"
---
# <a name="trottersteporacle-function"></a><span data-ttu-id="bece2-102">Trottersteporacle-Funktion</span><span class="sxs-lookup"><span data-stu-id="bece2-102">TrotterStepOracle function</span></span>

<span data-ttu-id="bece2-103">Namespace: [Microsoft. Quantum. Chemistry. jordanwigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="bece2-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="bece2-104">Paket: [Microsoft. Quantum. Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="bece2-104">Package: [Microsoft.Quantum.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span></span>


<span data-ttu-id="bece2-105">Gibt den Vorgang des trockschrittes und die für die Ausführung erforderlichen Parameter zurück.</span><span class="sxs-lookup"><span data-stu-id="bece2-105">Returns Trotter step operation and the parameters necessary to run it.</span></span>

```qsharp
function TrotterStepOracle (qSharpData : Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerEncodingData, trotterStepSize : Double, trotterOrder : Int) : (Int, (Double, (Qubit[] => Unit is Adj + Ctl)))
```


## <a name="input"></a><span data-ttu-id="bece2-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="bece2-106">Input</span></span>

### <a name="qsharpdata--jordanwignerencodingdata"></a><span data-ttu-id="bece2-107">qsharpdata: [jordanwignerencodingdata](xref:Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerEncodingData)</span><span class="sxs-lookup"><span data-stu-id="bece2-107">qSharpData : [JordanWignerEncodingData](xref:Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerEncodingData)</span></span>

<span data-ttu-id="bece2-108">Hamiltona wird nach `JordanWignerEncodingData` Format beschrieben.</span><span class="sxs-lookup"><span data-stu-id="bece2-108">Hamiltonian described by `JordanWignerEncodingData` format.</span></span>


### <a name="trotterstepsize--double"></a><span data-ttu-id="bece2-109">trotterstepsize: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="bece2-109">trotterStepSize : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="bece2-110">Schrittgröße des trotterintegrator.</span><span class="sxs-lookup"><span data-stu-id="bece2-110">Step size of Trotter integrator.</span></span>


### <a name="trotterorder--int"></a><span data-ttu-id="bece2-111">trotterorder: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="bece2-111">trotterOrder : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="bece2-112">Reihenfolge des trockintegrator.</span><span class="sxs-lookup"><span data-stu-id="bece2-112">Order of Trotter integrator.</span></span>



## <a name="output--intdoublequbit--unit--is-adj--ctl"></a><span data-ttu-id="bece2-113">Ausgabe: ([int](xref:microsoft.quantum.lang-ref.int), ([Double](xref:microsoft.quantum.lang-ref.double),[Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL))</span><span class="sxs-lookup"><span data-stu-id="bece2-113">Output : ([Int](xref:microsoft.quantum.lang-ref.int),([Double](xref:microsoft.quantum.lang-ref.double),[Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl))</span></span>

<span data-ttu-id="bece2-114">Ein Tupel, wobei: `Int` die Anzahl der zugeordneten Qubits ist, `Double` `1.0/trotterStepSize` und der Vorgang ist der trockschritt.</span><span class="sxs-lookup"><span data-stu-id="bece2-114">A tuple where: `Int` is the number of qubits allocated, `Double` is `1.0/trotterStepSize`, and the operation is the Trotter step.</span></span>