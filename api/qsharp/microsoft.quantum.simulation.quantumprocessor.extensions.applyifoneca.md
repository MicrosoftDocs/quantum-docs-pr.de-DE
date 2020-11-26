---
uid: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions.ApplyIfOneCA
title: Applyifoneca-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions
qsharp.name: ApplyIfOneCA
qsharp.summary: ''
ms.openlocfilehash: e997cf4b20fdd2c52285191b732297ca99886c22
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96230938"
---
# <a name="applyifoneca-operation"></a><span data-ttu-id="3c2a6-102">Applyifoneca-Vorgang</span><span class="sxs-lookup"><span data-stu-id="3c2a6-102">ApplyIfOneCA operation</span></span>

<span data-ttu-id="3c2a6-103">Namespace: [Microsoft. Quantum. Simulation. quantumprocessor. Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span><span class="sxs-lookup"><span data-stu-id="3c2a6-103">Namespace: [Microsoft.Quantum.Simulation.QuantumProcessor.Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span></span>

<span data-ttu-id="3c2a6-104">Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="3c2a6-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>




```qsharp
operation ApplyIfOneCA<'T> (measurementResult : Result, (onResultOneOp : ('T => Unit is Ctl + Adj), oneArg : 'T)) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="3c2a6-105">Eingabe</span><span class="sxs-lookup"><span data-stu-id="3c2a6-105">Input</span></span>

### <a name="measurementresult--__invalidresult__"></a><span data-ttu-id="3c2a6-106">messrementresult: __ungültig <Result>__</span><span class="sxs-lookup"><span data-stu-id="3c2a6-106">measurementResult : __invalid<Result>__</span></span>




### <a name="onresultoneop--t--unit--is-adj--ctl"></a><span data-ttu-id="3c2a6-107">onresultoneop: 't => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="3c2a6-107">onResultOneOp : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>




### <a name="onearg--t"></a><span data-ttu-id="3c2a6-108">onearg: 't</span><span class="sxs-lookup"><span data-stu-id="3c2a6-108">oneArg : 'T</span></span>





## <a name="output--unit"></a><span data-ttu-id="3c2a6-109">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="3c2a6-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="3c2a6-110">Typparameter</span><span class="sxs-lookup"><span data-stu-id="3c2a6-110">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="3c2a6-111">GIF</span><span class="sxs-lookup"><span data-stu-id="3c2a6-111">'T</span></span>

