---
uid: Microsoft.Quantum.Chemistry.JordanWigner._ApplyJordanWigner0123Term_
title: _ApplyJordanWigner0123Term_ -Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: _ApplyJordanWigner0123Term_
qsharp.summary: Applies time-evolution by a PQRS term described by a `GeneratorIndex`.
ms.openlocfilehash: 36590b2ee9f6f6c2b5e076f8e334dfe7b0144e5e
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703547"
---
# <a name="_applyjordanwigner0123term_-operation"></a><span data-ttu-id="feeca-102">_ApplyJordanWigner0123Term_ -Vorgang</span><span class="sxs-lookup"><span data-stu-id="feeca-102">_ApplyJordanWigner0123Term_ operation</span></span>

<span data-ttu-id="feeca-103">Namespace: [Microsoft. Quantum. Chemistry. jordanwigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="feeca-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="feeca-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="feeca-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="feeca-105">Wendet Time-Evolution durch einen pqrs-Begriff an, der von einem beschrieben wird `GeneratorIndex` .</span><span class="sxs-lookup"><span data-stu-id="feeca-105">Applies time-evolution by a PQRS term described by a `GeneratorIndex`.</span></span>

```qsharp
operation _ApplyJordanWigner0123Term_ (term : Microsoft.Quantum.Simulation.GeneratorIndex, stepSize : Double, qubits : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="feeca-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="feeca-106">Input</span></span>

### <a name="term--generatorindex"></a><span data-ttu-id="feeca-107">Begriff: [generatorindex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="feeca-107">term : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="feeca-108">`GeneratorIndex` der einen pqrs-Begriff darstellt.</span><span class="sxs-lookup"><span data-stu-id="feeca-108">`GeneratorIndex` representing a PQRS term.</span></span>


### <a name="stepsize--double"></a><span data-ttu-id="feeca-109">stepSize: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="feeca-109">stepSize : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="feeca-110">Dauer der Zeitentwicklung.</span><span class="sxs-lookup"><span data-stu-id="feeca-110">Duration of time-evolution.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="feeca-111">Qubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="feeca-111">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="feeca-112">Qubits von hamiltonan.</span><span class="sxs-lookup"><span data-stu-id="feeca-112">Qubits of Hamiltonian.</span></span>



## <a name="output--unit"></a><span data-ttu-id="feeca-113">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="feeca-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

