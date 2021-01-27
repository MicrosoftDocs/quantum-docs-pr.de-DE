---
uid: Microsoft.Quantum.Chemistry.JordanWigner._ApplyJordanWignerZZTerm_
title: _Applyjordanwignerzzterm_ -Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: _ApplyJordanWignerZZTerm_
qsharp.summary: Applies time-evolution by a ZZ term described by a `GeneratorIndex`.
ms.openlocfilehash: 4ecf6279595d12d4262aa6786d908270707b95bc
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98851684"
---
# <a name="_applyjordanwignerzzterm_-operation"></a><span data-ttu-id="9f6e9-102">_Applyjordanwignerzzterm_ -Vorgang</span><span class="sxs-lookup"><span data-stu-id="9f6e9-102">_ApplyJordanWignerZZTerm_ operation</span></span>

<span data-ttu-id="9f6e9-103">Namespace: [Microsoft. Quantum. Chemistry. jordanwigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="9f6e9-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="9f6e9-104">Paket: [Microsoft. Quantum. Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="9f6e9-104">Package: [Microsoft.Quantum.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span></span>


<span data-ttu-id="9f6e9-105">Wendet Time-Evolution um einen von einem beschriebenen ZZ-Begriff an `GeneratorIndex` .</span><span class="sxs-lookup"><span data-stu-id="9f6e9-105">Applies time-evolution by a ZZ term described by a `GeneratorIndex`.</span></span>

```qsharp
operation _ApplyJordanWignerZZTerm_ (term : Microsoft.Quantum.Simulation.GeneratorIndex, stepSize : Double, qubits : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="9f6e9-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="9f6e9-106">Input</span></span>

### <a name="term--generatorindex"></a><span data-ttu-id="9f6e9-107">Begriff: [generatorindex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="9f6e9-107">term : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="9f6e9-108">`GeneratorIndex` , der einen ZZ-Begriff darstellt.</span><span class="sxs-lookup"><span data-stu-id="9f6e9-108">`GeneratorIndex` representing a ZZ term.</span></span>


### <a name="stepsize--double"></a><span data-ttu-id="9f6e9-109">stepSize: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="9f6e9-109">stepSize : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="9f6e9-110">Dauer der Zeitentwicklung.</span><span class="sxs-lookup"><span data-stu-id="9f6e9-110">Duration of time-evolution.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="9f6e9-111">Qubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="9f6e9-111">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="9f6e9-112">Qubits von hamiltonan.</span><span class="sxs-lookup"><span data-stu-id="9f6e9-112">Qubits of Hamiltonian.</span></span>



## <a name="output--unit"></a><span data-ttu-id="9f6e9-113">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="9f6e9-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

