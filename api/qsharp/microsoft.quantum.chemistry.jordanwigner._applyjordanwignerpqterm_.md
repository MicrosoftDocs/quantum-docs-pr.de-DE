---
uid: Microsoft.Quantum.Chemistry.JordanWigner._ApplyJordanWignerPQTerm_
title: _Applyjordanwignerpqterm_ -Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: _ApplyJordanWignerPQTerm_
qsharp.summary: Applies time-evolution by a PQ term described by a `GeneratorIndex`.
ms.openlocfilehash: 6e7d3e422ea751371eeb3111dce88acc6eaf3b62
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98851714"
---
# <a name="_applyjordanwignerpqterm_-operation"></a><span data-ttu-id="d3a77-102">_Applyjordanwignerpqterm_ -Vorgang</span><span class="sxs-lookup"><span data-stu-id="d3a77-102">_ApplyJordanWignerPQTerm_ operation</span></span>

<span data-ttu-id="d3a77-103">Namespace: [Microsoft. Quantum. Chemistry. jordanwigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="d3a77-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="d3a77-104">Paket: [Microsoft. Quantum. Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="d3a77-104">Package: [Microsoft.Quantum.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span></span>


<span data-ttu-id="d3a77-105">Wendet Time-Evolution durch einen PQ-Begriff an, der von einem beschrieben wird `GeneratorIndex` .</span><span class="sxs-lookup"><span data-stu-id="d3a77-105">Applies time-evolution by a PQ term described by a `GeneratorIndex`.</span></span>

```qsharp
operation _ApplyJordanWignerPQTerm_ (term : Microsoft.Quantum.Simulation.GeneratorIndex, stepSize : Double, extraParityQubits : Qubit[], qubits : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="d3a77-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d3a77-106">Input</span></span>

### <a name="term--generatorindex"></a><span data-ttu-id="d3a77-107">Begriff: [generatorindex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="d3a77-107">term : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="d3a77-108">`GeneratorIndex` , der einen PQ-Begriff darstellt.</span><span class="sxs-lookup"><span data-stu-id="d3a77-108">`GeneratorIndex` representing a PQ term.</span></span>


### <a name="stepsize--double"></a><span data-ttu-id="d3a77-109">stepSize: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="d3a77-109">stepSize : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="d3a77-110">Dauer der Zeitentwicklung.</span><span class="sxs-lookup"><span data-stu-id="d3a77-110">Duration of time-evolution.</span></span>


### <a name="extraparityqubits--qubit"></a><span data-ttu-id="d3a77-111">extraparameityqubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="d3a77-111">extraParityQubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="d3a77-112">Optionale parbits, die das Vorzeichen der Time-Evolution kippen.</span><span class="sxs-lookup"><span data-stu-id="d3a77-112">Optional parity qubits that flip the sign of time-evolution.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="d3a77-113">Qubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="d3a77-113">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="d3a77-114">Qubits von hamiltonan.</span><span class="sxs-lookup"><span data-stu-id="d3a77-114">Qubits of Hamiltonian.</span></span>



## <a name="output--unit"></a><span data-ttu-id="d3a77-115">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="d3a77-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

