---
uid: Microsoft.Quantum.Chemistry.JordanWigner._ApplyJordanWignerPQandPQQRTerm_
title: _Applyjordanwignerpqandpqqrterm_ -Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: _ApplyJordanWignerPQandPQQRTerm_
qsharp.summary: Applies time-evolution by a PQ or PQQR term described by a `GeneratorIndex`.
ms.openlocfilehash: 8b6d022c70052a91d3cf6d4549db5ed1434d3fc8
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96203976"
---
# <a name="_applyjordanwignerpqandpqqrterm_-operation"></a><span data-ttu-id="97ebe-102">_Applyjordanwignerpqandpqqrterm_ -Vorgang</span><span class="sxs-lookup"><span data-stu-id="97ebe-102">_ApplyJordanWignerPQandPQQRTerm_ operation</span></span>

<span data-ttu-id="97ebe-103">Namespace: [Microsoft. Quantum. Chemistry. jordanwigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="97ebe-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="97ebe-104">Paket: [Microsoft. Quantum. Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="97ebe-104">Package: [Microsoft.Quantum.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span></span>


<span data-ttu-id="97ebe-105">Wendet Time-Evolution durch einen PQ-oder pqqr-Begriff an, der von einem beschrieben wird `GeneratorIndex` .</span><span class="sxs-lookup"><span data-stu-id="97ebe-105">Applies time-evolution by a PQ or PQQR term described by a `GeneratorIndex`.</span></span>

```qsharp
operation _ApplyJordanWignerPQandPQQRTerm_ (term : Microsoft.Quantum.Simulation.GeneratorIndex, stepSize : Double, qubits : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="97ebe-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="97ebe-106">Input</span></span>

### <a name="term--generatorindex"></a><span data-ttu-id="97ebe-107">Begriff: [generatorindex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="97ebe-107">term : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="97ebe-108">`GeneratorIndex` , der einen PQ-oder pqqr-Begriff darstellt.</span><span class="sxs-lookup"><span data-stu-id="97ebe-108">`GeneratorIndex` representing a PQ or PQQR term.</span></span>


### <a name="stepsize--double"></a><span data-ttu-id="97ebe-109">stepSize: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="97ebe-109">stepSize : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="97ebe-110">Dauer der Zeitentwicklung.</span><span class="sxs-lookup"><span data-stu-id="97ebe-110">Duration of time-evolution.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="97ebe-111">Qubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="97ebe-111">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="97ebe-112">Qubits von hamiltonan.</span><span class="sxs-lookup"><span data-stu-id="97ebe-112">Qubits of Hamiltonian.</span></span>



## <a name="output--unit"></a><span data-ttu-id="97ebe-113">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="97ebe-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

