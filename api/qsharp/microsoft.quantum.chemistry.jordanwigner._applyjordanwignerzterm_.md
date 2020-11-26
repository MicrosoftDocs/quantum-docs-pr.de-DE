---
uid: Microsoft.Quantum.Chemistry.JordanWigner._ApplyJordanWignerZTerm_
title: _Applyjordanwignerzterm_ -Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: _ApplyJordanWignerZTerm_
qsharp.summary: Applies time-evolution by a Z term described by a `GeneratorIndex`.
ms.openlocfilehash: ad9245b0fd79b4f383d1ef8531537b03d78ae9b8
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96203993"
---
# <a name="_applyjordanwignerzterm_-operation"></a><span data-ttu-id="de26f-102">_Applyjordanwignerzterm_ -Vorgang</span><span class="sxs-lookup"><span data-stu-id="de26f-102">_ApplyJordanWignerZTerm_ operation</span></span>

<span data-ttu-id="de26f-103">Namespace: [Microsoft. Quantum. Chemistry. jordanwigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="de26f-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="de26f-104">Paket: [Microsoft. Quantum. Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="de26f-104">Package: [Microsoft.Quantum.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span></span>


<span data-ttu-id="de26f-105">Wendet Time-Evolution um einen Z-Begriff an, der von einem beschrieben wird `GeneratorIndex` .</span><span class="sxs-lookup"><span data-stu-id="de26f-105">Applies time-evolution by a Z term described by a `GeneratorIndex`.</span></span>

```qsharp
operation _ApplyJordanWignerZTerm_ (term : Microsoft.Quantum.Simulation.GeneratorIndex, stepSize : Double, qubits : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="de26f-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="de26f-106">Input</span></span>

### <a name="term--generatorindex"></a><span data-ttu-id="de26f-107">Begriff: [generatorindex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="de26f-107">term : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="de26f-108">`GeneratorIndex` , der einen Z-Begriff darstellt.</span><span class="sxs-lookup"><span data-stu-id="de26f-108">`GeneratorIndex` representing a Z term.</span></span>


### <a name="stepsize--double"></a><span data-ttu-id="de26f-109">stepSize: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="de26f-109">stepSize : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="de26f-110">Dauer der Zeitentwicklung.</span><span class="sxs-lookup"><span data-stu-id="de26f-110">Duration of time-evolution.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="de26f-111">Qubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="de26f-111">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="de26f-112">Qubits von hamiltonan.</span><span class="sxs-lookup"><span data-stu-id="de26f-112">Qubits of Hamiltonian.</span></span>



## <a name="output--unit"></a><span data-ttu-id="de26f-113">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="de26f-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

