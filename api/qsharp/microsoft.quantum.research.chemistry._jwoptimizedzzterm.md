---
uid: Microsoft.Quantum.Research.Chemistry._JWOptimizedZZTerm
title: _JWOptimizedZZTerm Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Research.Chemistry
qsharp.name: _JWOptimizedZZTerm
qsharp.summary: Applies time-evolution by a ZZ term described by a `GeneratorIndex`.
ms.openlocfilehash: e12d146c0f706e960294580ad4b26ca83711ce33
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98844356"
---
# <a name="_jwoptimizedzzterm-operation"></a><span data-ttu-id="d9639-102">_JWOptimizedZZTerm Vorgang</span><span class="sxs-lookup"><span data-stu-id="d9639-102">_JWOptimizedZZTerm operation</span></span>

<span data-ttu-id="d9639-103">Namespace: [Microsoft. Quantum. Research. Chemistry](xref:Microsoft.Quantum.Research.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="d9639-103">Namespace: [Microsoft.Quantum.Research.Chemistry](xref:Microsoft.Quantum.Research.Chemistry)</span></span>

<span data-ttu-id="d9639-104">Paket: [Microsoft. Quantum. Research. Chemistry](https://nuget.org/packages/Microsoft.Quantum.Research.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="d9639-104">Package: [Microsoft.Quantum.Research.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Research.Chemistry)</span></span>


<span data-ttu-id="d9639-105">Wendet Time-Evolution um einen von einem beschriebenen ZZ-Begriff an `GeneratorIndex` .</span><span class="sxs-lookup"><span data-stu-id="d9639-105">Applies time-evolution by a ZZ term described by a `GeneratorIndex`.</span></span>

```qsharp
operation _JWOptimizedZZTerm (term : Microsoft.Quantum.Simulation.GeneratorIndex, stepSize : Double, parityQubit : Qubit, qubits : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="d9639-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d9639-106">Input</span></span>

### <a name="term--generatorindex"></a><span data-ttu-id="d9639-107">Begriff: [generatorindex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="d9639-107">term : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="d9639-108">`GeneratorIndex` , der einen ZZ-Begriff darstellt.</span><span class="sxs-lookup"><span data-stu-id="d9639-108">`GeneratorIndex` representing a ZZ term.</span></span>


### <a name="stepsize--double"></a><span data-ttu-id="d9639-109">stepSize: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="d9639-109">stepSize : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="d9639-110">Dauer der Zeitentwicklung.</span><span class="sxs-lookup"><span data-stu-id="d9639-110">Duration of time-evolution.</span></span>


### <a name="parityqubit--qubit"></a><span data-ttu-id="d9639-111">parameteryqubit: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="d9639-111">parityQubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="d9639-112">Qubit, das das Vorzeichen der Zeitentwicklung bestimmt.</span><span class="sxs-lookup"><span data-stu-id="d9639-112">Qubit that determines the sign of time-evolution.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="d9639-113">Qubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="d9639-113">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="d9639-114">Qubits von hamiltonan.</span><span class="sxs-lookup"><span data-stu-id="d9639-114">Qubits of Hamiltonian.</span></span>



## <a name="output--unit"></a><span data-ttu-id="d9639-115">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="d9639-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

