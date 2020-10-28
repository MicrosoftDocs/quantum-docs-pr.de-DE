---
uid: Microsoft.Quantum.Chemistry.JordanWigner._ApplyJordanWignerZZTerm_
title: _Applyjordanwignerzzterm_ -Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: _ApplyJordanWignerZZTerm_
qsharp.summary: Applies time-evolution by a ZZ term described by a `GeneratorIndex`.
ms.openlocfilehash: 9f03255d53f7ed7f3e79689ea53c8b95133f6cde
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703505"
---
# <a name="_applyjordanwignerzzterm_-operation"></a><span data-ttu-id="90507-102">_Applyjordanwignerzzterm_ -Vorgang</span><span class="sxs-lookup"><span data-stu-id="90507-102">_ApplyJordanWignerZZTerm_ operation</span></span>

<span data-ttu-id="90507-103">Namespace: [Microsoft. Quantum. Chemistry. jordanwigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="90507-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="90507-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="90507-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="90507-105">Wendet Time-Evolution um einen von einem beschriebenen ZZ-Begriff an `GeneratorIndex` .</span><span class="sxs-lookup"><span data-stu-id="90507-105">Applies time-evolution by a ZZ term described by a `GeneratorIndex`.</span></span>

```qsharp
operation _ApplyJordanWignerZZTerm_ (term : Microsoft.Quantum.Simulation.GeneratorIndex, stepSize : Double, qubits : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="90507-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="90507-106">Input</span></span>

### <a name="term--generatorindex"></a><span data-ttu-id="90507-107">Begriff: [generatorindex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="90507-107">term : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="90507-108">`GeneratorIndex` , der einen ZZ-Begriff darstellt.</span><span class="sxs-lookup"><span data-stu-id="90507-108">`GeneratorIndex` representing a ZZ term.</span></span>


### <a name="stepsize--double"></a><span data-ttu-id="90507-109">stepSize: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="90507-109">stepSize : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="90507-110">Dauer der Zeitentwicklung.</span><span class="sxs-lookup"><span data-stu-id="90507-110">Duration of time-evolution.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="90507-111">Qubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="90507-111">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="90507-112">Qubits von hamiltonan.</span><span class="sxs-lookup"><span data-stu-id="90507-112">Qubits of Hamiltonian.</span></span>



## <a name="output--unit"></a><span data-ttu-id="90507-113">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="90507-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

