---
uid: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions.ApplyIfElseRC
title: Applyifelserc-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions
qsharp.name: ApplyIfElseRC
qsharp.summary: ''
ms.openlocfilehash: 97536f2071918bec7129d8157e8750a5c310767f
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855649"
---
# <a name="applyifelserc-operation"></a><span data-ttu-id="ac4b2-102">Applyifelserc-Vorgang</span><span class="sxs-lookup"><span data-stu-id="ac4b2-102">ApplyIfElseRC operation</span></span>

<span data-ttu-id="ac4b2-103">Namespace: [Microsoft. Quantum. Simulation. quantumprocessor. Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span><span class="sxs-lookup"><span data-stu-id="ac4b2-103">Namespace: [Microsoft.Quantum.Simulation.QuantumProcessor.Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span></span>

<span data-ttu-id="ac4b2-104">Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="ac4b2-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>




```qsharp
operation ApplyIfElseRC<'T, 'U> (measurementResult : Result, (onResultZeroOp : ('T => Unit is Ctl), zeroArg : 'T), (onResultOneOp : ('U => Unit is Ctl), oneArg : 'U)) : Unit is Ctl
```


## <a name="input"></a><span data-ttu-id="ac4b2-105">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ac4b2-105">Input</span></span>

### <a name="measurementresult--__invalidresult__"></a><span data-ttu-id="ac4b2-106">messrementresult: __ungültig <Result>__</span><span class="sxs-lookup"><span data-stu-id="ac4b2-106">measurementResult : __invalid<Result>__</span></span>




### <a name="onresultzeroop--t--unit--is-ctl"></a><span data-ttu-id="ac4b2-107">onresultzeroop: 't => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist CTL</span><span class="sxs-lookup"><span data-stu-id="ac4b2-107">onResultZeroOp : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>




### <a name="zeroarg--t"></a><span data-ttu-id="ac4b2-108">NULL: nicht</span><span class="sxs-lookup"><span data-stu-id="ac4b2-108">zeroArg : 'T</span></span>




### <a name="onresultoneop--u--unit--is-ctl"></a><span data-ttu-id="ac4b2-109">onresultoneop: "U => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist CTL</span><span class="sxs-lookup"><span data-stu-id="ac4b2-109">onResultOneOp : 'U => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>




### <a name="onearg--u"></a><span data-ttu-id="ac4b2-110">onearg: "U</span><span class="sxs-lookup"><span data-stu-id="ac4b2-110">oneArg : 'U</span></span>





## <a name="output--unit"></a><span data-ttu-id="ac4b2-111">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="ac4b2-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="ac4b2-112">Typparameter</span><span class="sxs-lookup"><span data-stu-id="ac4b2-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="ac4b2-113">GIF</span><span class="sxs-lookup"><span data-stu-id="ac4b2-113">'T</span></span>


### <a name="u"></a><span data-ttu-id="ac4b2-114">"U</span><span class="sxs-lookup"><span data-stu-id="ac4b2-114">'U</span></span>

