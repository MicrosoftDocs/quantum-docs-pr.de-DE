---
uid: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions.ApplyIfOne
title: Applyifone-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions
qsharp.name: ApplyIfOne
qsharp.summary: ''
ms.openlocfilehash: f8f4f3b05d3986d94e6f1be380d6c83151d87f17
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96230666"
---
# <a name="applyifone-operation"></a><span data-ttu-id="963cc-102">Applyifone-Vorgang</span><span class="sxs-lookup"><span data-stu-id="963cc-102">ApplyIfOne operation</span></span>

<span data-ttu-id="963cc-103">Namespace: [Microsoft. Quantum. Simulation. quantumprocessor. Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span><span class="sxs-lookup"><span data-stu-id="963cc-103">Namespace: [Microsoft.Quantum.Simulation.QuantumProcessor.Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span></span>

<span data-ttu-id="963cc-104">Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="963cc-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>




```qsharp
operation ApplyIfOne<'T> (measurementResult : Result, (onResultOneOp : ('T => Unit), oneArg : 'T)) : Unit
```


## <a name="input"></a><span data-ttu-id="963cc-105">Eingabe</span><span class="sxs-lookup"><span data-stu-id="963cc-105">Input</span></span>

### <a name="measurementresult--__invalidresult__"></a><span data-ttu-id="963cc-106">messrementresult: __ungültig <Result>__</span><span class="sxs-lookup"><span data-stu-id="963cc-106">measurementResult : __invalid<Result>__</span></span>




### <a name="onresultoneop--t--unit"></a><span data-ttu-id="963cc-107">onresultoneop: 't => [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="963cc-107">onResultOneOp : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 




### <a name="onearg--t"></a><span data-ttu-id="963cc-108">onearg: 't</span><span class="sxs-lookup"><span data-stu-id="963cc-108">oneArg : 'T</span></span>





## <a name="output--unit"></a><span data-ttu-id="963cc-109">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="963cc-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="963cc-110">Typparameter</span><span class="sxs-lookup"><span data-stu-id="963cc-110">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="963cc-111">GIF</span><span class="sxs-lookup"><span data-stu-id="963cc-111">'T</span></span>

