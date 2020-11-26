---
uid: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions.ApplyConditionally
title: Applybedingt-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions
qsharp.name: ApplyConditionally
qsharp.summary: ''
ms.openlocfilehash: 24d52576d2fb3e83f294874be4b0d1cd6a80f188
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96229068"
---
# <a name="applyconditionally-operation"></a><span data-ttu-id="6cc46-102">Applybedingt-Vorgang</span><span class="sxs-lookup"><span data-stu-id="6cc46-102">ApplyConditionally operation</span></span>

<span data-ttu-id="6cc46-103">Namespace: [Microsoft. Quantum. Simulation. quantumprocessor. Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span><span class="sxs-lookup"><span data-stu-id="6cc46-103">Namespace: [Microsoft.Quantum.Simulation.QuantumProcessor.Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span></span>

<span data-ttu-id="6cc46-104">Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="6cc46-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>




```qsharp
operation ApplyConditionally<'T, 'U> (measurementResults : Result[], resultsValues : Result[], (onEqualOp : ('T => Unit), equalArg : 'T), (onNonEqualOp : ('U => Unit), nonEqualArg : 'U)) : Unit
```


## <a name="input"></a><span data-ttu-id="6cc46-105">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6cc46-105">Input</span></span>

### <a name="measurementresults--__invalidresult__"></a><span data-ttu-id="6cc46-106">"messrementresults": __ungültig <Result>__[]</span><span class="sxs-lookup"><span data-stu-id="6cc46-106">measurementResults : __invalid<Result>__[]</span></span>




### <a name="resultsvalues--__invalidresult__"></a><span data-ttu-id="6cc46-107">result values: __ungültig <Result>__[]</span><span class="sxs-lookup"><span data-stu-id="6cc46-107">resultsValues : __invalid<Result>__[]</span></span>




### <a name="onequalop--t--unit"></a><span data-ttu-id="6cc46-108">onequalop: 't => [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="6cc46-108">onEqualOp : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 




### <a name="equalarg--t"></a><span data-ttu-id="6cc46-109">equalarg: 't</span><span class="sxs-lookup"><span data-stu-id="6cc46-109">equalArg : 'T</span></span>




### <a name="onnonequalop--u--unit"></a><span data-ttu-id="6cc46-110">onnonequalop: ' U => [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="6cc46-110">onNonEqualOp : 'U => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 




### <a name="nonequalarg--u"></a><span data-ttu-id="6cc46-111">nicht equalarg: "U</span><span class="sxs-lookup"><span data-stu-id="6cc46-111">nonEqualArg : 'U</span></span>





## <a name="output--unit"></a><span data-ttu-id="6cc46-112">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="6cc46-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="6cc46-113">Typparameter</span><span class="sxs-lookup"><span data-stu-id="6cc46-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="6cc46-114">GIF</span><span class="sxs-lookup"><span data-stu-id="6cc46-114">'T</span></span>


### <a name="u"></a><span data-ttu-id="6cc46-115">"U</span><span class="sxs-lookup"><span data-stu-id="6cc46-115">'U</span></span>

