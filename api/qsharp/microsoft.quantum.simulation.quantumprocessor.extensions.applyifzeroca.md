---
uid: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions.ApplyIfZeroCA
title: Applyif nuloca-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions
qsharp.name: ApplyIfZeroCA
qsharp.summary: ''
ms.openlocfilehash: 978964888a89ca46847ae7aa01a2c180ee322436
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92725677"
---
# <a name="applyifzeroca-operation"></a><span data-ttu-id="e6101-102">Applyif nuloca-Vorgang</span><span class="sxs-lookup"><span data-stu-id="e6101-102">ApplyIfZeroCA operation</span></span>

<span data-ttu-id="e6101-103">Namespace: [Microsoft. Quantum. Simulation. quantumprocessor. Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span><span class="sxs-lookup"><span data-stu-id="e6101-103">Namespace: [Microsoft.Quantum.Simulation.QuantumProcessor.Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span></span>

<span data-ttu-id="e6101-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="e6101-104">Package: [](https://nuget.org/packages/)</span></span>




```qsharp
operation ApplyIfZeroCA<'T> (measurementResult : Result, (onResultZeroOp : ('T => Unit is Ctl + Adj), zeroArg : 'T)) : Unit
```


## <a name="input"></a><span data-ttu-id="e6101-105">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e6101-105">Input</span></span>

### <a name="measurementresult--__invalidresult__"></a><span data-ttu-id="e6101-106">messrementresult: __ungültig <Result>__</span><span class="sxs-lookup"><span data-stu-id="e6101-106">measurementResult : __invalid<Result>__</span></span>




### <a name="onresultzeroop--t--unit-ctl--adj"></a><span data-ttu-id="e6101-107">onresultzeroop: 't => [Unit](xref:microsoft.quantum.lang-ref.unit) CTL + ADJ</span><span class="sxs-lookup"><span data-stu-id="e6101-107">onResultZeroOp : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl + Adj</span></span>




### <a name="zeroarg--t"></a><span data-ttu-id="e6101-108">NULL: nicht</span><span class="sxs-lookup"><span data-stu-id="e6101-108">zeroArg : 'T</span></span>





## <a name="output--unit"></a><span data-ttu-id="e6101-109">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="e6101-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="e6101-110">Typparameter</span><span class="sxs-lookup"><span data-stu-id="e6101-110">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="e6101-111">GIF</span><span class="sxs-lookup"><span data-stu-id="e6101-111">'T</span></span>

