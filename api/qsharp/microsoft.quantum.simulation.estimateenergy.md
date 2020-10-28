---
uid: Microsoft.Quantum.Simulation.EstimateEnergy
title: Estimateenergy-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: EstimateEnergy
qsharp.summary: Performs state preparation by applying a `statePrepUnitary` on an automatically allocated input state phase estimation with respect to `qpeUnitary`on the resulting state using a `phaseEstAlgorithm`.
ms.openlocfilehash: ba4a5372aaf092c3ac3a1302f9715ca643be8436
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92722052"
---
# <a name="estimateenergy-operation"></a><span data-ttu-id="43795-102">Estimateenergy-Vorgang</span><span class="sxs-lookup"><span data-stu-id="43795-102">EstimateEnergy operation</span></span>

<span data-ttu-id="43795-103">Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="43795-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="43795-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="43795-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="43795-105">Führt die Zustands Vorbereitung durch Anwenden eines `statePrepUnitary` auf eine automatisch zugeordnete Eingabe Zustands-Phasen Schätzung in Bezug auf `qpeUnitary` den resultierenden Zustand mithilfe von aus `phaseEstAlgorithm` .</span><span class="sxs-lookup"><span data-stu-id="43795-105">Performs state preparation by applying a `statePrepUnitary` on an automatically allocated input state phase estimation with respect to `qpeUnitary`on the resulting state using a `phaseEstAlgorithm`.</span></span>

```qsharp
operation EstimateEnergy (nQubits : Int, statePrepUnitary : (Qubit[] => Unit), qpeUnitary : (Qubit[] => Unit is Adj + Ctl), phaseEstAlgorithm : ((Microsoft.Quantum.Oracles.DiscreteOracle, Qubit[]) => Double)) : Double
```


## <a name="input"></a><span data-ttu-id="43795-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="43795-106">Input</span></span>

### <a name="nqubits--int"></a><span data-ttu-id="43795-107">nqubits: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="43795-107">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="43795-108">Die Anzahl der zum Ausführen der Simulation verwendeten Qubits.</span><span class="sxs-lookup"><span data-stu-id="43795-108">Number of qubits used to perform simulation.</span></span>


### <a name="stateprepunitary--qubit--unit"></a><span data-ttu-id="43795-109">stateprepeinheitlicher: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="43795-109">statePrepUnitary : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="43795-110">Ein Oracle, das die Zustands Vorbereitung für den ursprünglichen Dynamical-Generator darstellt.</span><span class="sxs-lookup"><span data-stu-id="43795-110">An oracle representing state preparation for the initial dynamical generator.</span></span>


### <a name="qpeunitary--qubit--unit-adj--ctl"></a><span data-ttu-id="43795-111">qpeer einheitlich: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Einheit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="43795-111">qpeUnitary : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="43795-112">Ein Oracle, das einen einheitlichen Operator $U $ darstellt, der die Entwicklung für "Time $ \delta t $" unter einem Dynamical Generator mit dem "Ground State $ \ket{\phi} $" und "Ground State Energy $E = \phi \\ , \delta t $" darstellt.</span><span class="sxs-lookup"><span data-stu-id="43795-112">An oracle representing a unitary operator $U$ representing evolution for time $\delta t$ under a dynamical generator with ground state $\ket{\phi}$ and ground state energy $E = \phi\\,\delta t$.</span></span>


### <a name="phaseestalgorithm--discreteoraclequbit--double"></a><span data-ttu-id="43795-113">phaseestalgorithmus: ([diskreteoracle](xref:Microsoft.Quantum.Oracles.DiscreteOracle),[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="43795-113">phaseEstAlgorithm : ([DiscreteOracle](xref:Microsoft.Quantum.Oracles.DiscreteOracle),[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Double](xref:microsoft.quantum.lang-ref.double)</span></span> 

<span data-ttu-id="43795-114">Ein Vorgang, der die Phasen Schätzung für einen angegebenen einheitlichen Vorgang ausführt.</span><span class="sxs-lookup"><span data-stu-id="43795-114">An operation that performs phase estimation on a given unitary operation.</span></span>
<span data-ttu-id="43795-115">Weitere Informationen finden Sie unter [iterative Phasen Schätzung](/quantum/libraries/characterization#iterative-phase-estimation) .</span><span class="sxs-lookup"><span data-stu-id="43795-115">See [iterative phase estimation](/quantum/libraries/characterization#iterative-phase-estimation) for more details.</span></span>



## <a name="output--double"></a><span data-ttu-id="43795-116">Ausgabe: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="43795-116">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="43795-117">Eine Schätzung von $ \hat{\phi} $ der Erde State Energy $ \phi $ der Boden Zustands Energie des Generators, der durch $U $ dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="43795-117">An estimate $\hat{\phi}$ of the ground state energy $\phi$ of the ground state energy of the generator represented by $U$.</span></span>