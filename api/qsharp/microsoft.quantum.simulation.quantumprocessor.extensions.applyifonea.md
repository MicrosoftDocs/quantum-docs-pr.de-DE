---
uid: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions.ApplyIfOneA
title: Applyifonea-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions
qsharp.name: ApplyIfOneA
qsharp.summary: ''
ms.openlocfilehash: 63ce44300f6e50cb91294b62611275e3e8942655
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855608"
---
# <a name="applyifonea-operation"></a><span data-ttu-id="3ae1b-102">Applyifonea-Vorgang</span><span class="sxs-lookup"><span data-stu-id="3ae1b-102">ApplyIfOneA operation</span></span>

<span data-ttu-id="3ae1b-103">Namespace: [Microsoft. Quantum. Simulation. quantumprocessor. Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span><span class="sxs-lookup"><span data-stu-id="3ae1b-103">Namespace: [Microsoft.Quantum.Simulation.QuantumProcessor.Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span></span>

<span data-ttu-id="3ae1b-104">Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="3ae1b-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>




```qsharp
operation ApplyIfOneA<'T> (measurementResult : Result, (onResultOneOp : ('T => Unit is Adj), oneArg : 'T)) : Unit is Adj
```


## <a name="input"></a><span data-ttu-id="3ae1b-105">Eingabe</span><span class="sxs-lookup"><span data-stu-id="3ae1b-105">Input</span></span>

### <a name="measurementresult--__invalidresult__"></a><span data-ttu-id="3ae1b-106">messrementresult: __ungültig <Result>__</span><span class="sxs-lookup"><span data-stu-id="3ae1b-106">measurementResult : __invalid<Result>__</span></span>




### <a name="onresultoneop--t--unit--is-adj"></a><span data-ttu-id="3ae1b-107">onresultoneop: 't => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ</span><span class="sxs-lookup"><span data-stu-id="3ae1b-107">onResultOneOp : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>




### <a name="onearg--t"></a><span data-ttu-id="3ae1b-108">onearg: 't</span><span class="sxs-lookup"><span data-stu-id="3ae1b-108">oneArg : 'T</span></span>





## <a name="output--unit"></a><span data-ttu-id="3ae1b-109">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="3ae1b-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="3ae1b-110">Typparameter</span><span class="sxs-lookup"><span data-stu-id="3ae1b-110">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="3ae1b-111">GIF</span><span class="sxs-lookup"><span data-stu-id="3ae1b-111">'T</span></span>

