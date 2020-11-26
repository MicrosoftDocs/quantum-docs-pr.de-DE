---
uid: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions.ApplyIfElseRCA
title: Applyifelserca-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions
qsharp.name: ApplyIfElseRCA
qsharp.summary: ''
ms.openlocfilehash: 6fbf186575775b3ae18a41727c225fb871f8dac0
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96192620"
---
# <a name="applyifelserca-operation"></a><span data-ttu-id="99cbf-102">Applyifelserca-Vorgang</span><span class="sxs-lookup"><span data-stu-id="99cbf-102">ApplyIfElseRCA operation</span></span>

<span data-ttu-id="99cbf-103">Namespace: [Microsoft. Quantum. Simulation. quantumprocessor. Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span><span class="sxs-lookup"><span data-stu-id="99cbf-103">Namespace: [Microsoft.Quantum.Simulation.QuantumProcessor.Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span></span>

<span data-ttu-id="99cbf-104">Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="99cbf-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>




```qsharp
operation ApplyIfElseRCA<'T, 'U> (measurementResult : Result, (onResultZeroOp : ('T => Unit is Adj + Ctl), zeroArg : 'T), (onResultOneOp : ('U => Unit is Adj + Ctl), oneArg : 'U)) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="99cbf-105">Eingabe</span><span class="sxs-lookup"><span data-stu-id="99cbf-105">Input</span></span>

### <a name="measurementresult--__invalidresult__"></a><span data-ttu-id="99cbf-106">messrementresult: __ungültig <Result>__</span><span class="sxs-lookup"><span data-stu-id="99cbf-106">measurementResult : __invalid<Result>__</span></span>




### <a name="onresultzeroop--t--unit--is-adj--ctl"></a><span data-ttu-id="99cbf-107">onresultzeroop: 't => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="99cbf-107">onResultZeroOp : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>




### <a name="zeroarg--t"></a><span data-ttu-id="99cbf-108">NULL: nicht</span><span class="sxs-lookup"><span data-stu-id="99cbf-108">zeroArg : 'T</span></span>




### <a name="onresultoneop--u--unit--is-adj--ctl"></a><span data-ttu-id="99cbf-109">onresultoneop: "U => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="99cbf-109">onResultOneOp : 'U => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>




### <a name="onearg--u"></a><span data-ttu-id="99cbf-110">onearg: "U</span><span class="sxs-lookup"><span data-stu-id="99cbf-110">oneArg : 'U</span></span>





## <a name="output--unit"></a><span data-ttu-id="99cbf-111">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="99cbf-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="99cbf-112">Typparameter</span><span class="sxs-lookup"><span data-stu-id="99cbf-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="99cbf-113">GIF</span><span class="sxs-lookup"><span data-stu-id="99cbf-113">'T</span></span>


### <a name="u"></a><span data-ttu-id="99cbf-114">"U</span><span class="sxs-lookup"><span data-stu-id="99cbf-114">'U</span></span>

