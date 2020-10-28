---
uid: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions.ApplyIfOneC
title: Applyifonec-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions
qsharp.name: ApplyIfOneC
qsharp.summary: ''
ms.openlocfilehash: 8456201d4ed137f3d84013f3b5170b52b27e66c5
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92725384"
---
# <a name="applyifonec-operation"></a><span data-ttu-id="c8e2f-102">Applyifonec-Vorgang</span><span class="sxs-lookup"><span data-stu-id="c8e2f-102">ApplyIfOneC operation</span></span>

<span data-ttu-id="c8e2f-103">Namespace: [Microsoft. Quantum. Simulation. quantumprocessor. Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span><span class="sxs-lookup"><span data-stu-id="c8e2f-103">Namespace: [Microsoft.Quantum.Simulation.QuantumProcessor.Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span></span>

<span data-ttu-id="c8e2f-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="c8e2f-104">Package: [](https://nuget.org/packages/)</span></span>




```qsharp
operation ApplyIfOneC<'T> (measurementResult : Result, (onResultOneOp : ('T => Unit is Ctl), oneArg : 'T)) : Unit
```


## <a name="input"></a><span data-ttu-id="c8e2f-105">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c8e2f-105">Input</span></span>

### <a name="measurementresult--__invalidresult__"></a><span data-ttu-id="c8e2f-106">messrementresult: __ungültig <Result>__</span><span class="sxs-lookup"><span data-stu-id="c8e2f-106">measurementResult : __invalid<Result>__</span></span>




### <a name="onresultoneop--t--unit-ctl"></a><span data-ttu-id="c8e2f-107">onresultoneop: 't => [Unit](xref:microsoft.quantum.lang-ref.unit) CTL</span><span class="sxs-lookup"><span data-stu-id="c8e2f-107">onResultOneOp : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>




### <a name="onearg--t"></a><span data-ttu-id="c8e2f-108">onearg: 't</span><span class="sxs-lookup"><span data-stu-id="c8e2f-108">oneArg : 'T</span></span>





## <a name="output--unit"></a><span data-ttu-id="c8e2f-109">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="c8e2f-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="c8e2f-110">Typparameter</span><span class="sxs-lookup"><span data-stu-id="c8e2f-110">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="c8e2f-111">GIF</span><span class="sxs-lookup"><span data-stu-id="c8e2f-111">'T</span></span>

