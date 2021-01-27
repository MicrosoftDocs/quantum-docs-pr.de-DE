---
uid: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions.ApplyConditionally
title: Applybedingt-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions
qsharp.name: ApplyConditionally
qsharp.summary: ''
ms.openlocfilehash: 67a4dcba5c193222c06ab429813adf12d7bbedfb
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98847896"
---
# <a name="applyconditionally-operation"></a><span data-ttu-id="97eaf-102">Applybedingt-Vorgang</span><span class="sxs-lookup"><span data-stu-id="97eaf-102">ApplyConditionally operation</span></span>

<span data-ttu-id="97eaf-103">Namespace: [Microsoft. Quantum. Simulation. quantumprocessor. Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span><span class="sxs-lookup"><span data-stu-id="97eaf-103">Namespace: [Microsoft.Quantum.Simulation.QuantumProcessor.Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span></span>

<span data-ttu-id="97eaf-104">Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="97eaf-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>




```qsharp
operation ApplyConditionally<'T, 'U> (measurementResults : Result[], resultsValues : Result[], (onEqualOp : ('T => Unit), equalArg : 'T), (onNonEqualOp : ('U => Unit), nonEqualArg : 'U)) : Unit
```


## <a name="input"></a><span data-ttu-id="97eaf-105">Eingabe</span><span class="sxs-lookup"><span data-stu-id="97eaf-105">Input</span></span>

### <a name="measurementresults--__invalidresult__"></a><span data-ttu-id="97eaf-106">"messrementresults": __ungültig <Result>__[]</span><span class="sxs-lookup"><span data-stu-id="97eaf-106">measurementResults : __invalid<Result>__[]</span></span>




### <a name="resultsvalues--__invalidresult__"></a><span data-ttu-id="97eaf-107">result values: __ungültig <Result>__[]</span><span class="sxs-lookup"><span data-stu-id="97eaf-107">resultsValues : __invalid<Result>__[]</span></span>




### <a name="onequalop--t--unit"></a><span data-ttu-id="97eaf-108">onequalop: 't => [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="97eaf-108">onEqualOp : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 




### <a name="equalarg--t"></a><span data-ttu-id="97eaf-109">equalarg: 't</span><span class="sxs-lookup"><span data-stu-id="97eaf-109">equalArg : 'T</span></span>




### <a name="onnonequalop--u--unit"></a><span data-ttu-id="97eaf-110">onnonequalop: ' U => [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="97eaf-110">onNonEqualOp : 'U => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 




### <a name="nonequalarg--u"></a><span data-ttu-id="97eaf-111">nicht equalarg: "U</span><span class="sxs-lookup"><span data-stu-id="97eaf-111">nonEqualArg : 'U</span></span>





## <a name="output--unit"></a><span data-ttu-id="97eaf-112">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="97eaf-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="97eaf-113">Typparameter</span><span class="sxs-lookup"><span data-stu-id="97eaf-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="97eaf-114">GIF</span><span class="sxs-lookup"><span data-stu-id="97eaf-114">'T</span></span>


### <a name="u"></a><span data-ttu-id="97eaf-115">"U</span><span class="sxs-lookup"><span data-stu-id="97eaf-115">'U</span></span>

