---
uid: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions.ApplyConditionallyC
title: Applyconditionallyc-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions
qsharp.name: ApplyConditionallyC
qsharp.summary: ''
ms.openlocfilehash: fc1cf50b7befd40cf20720032329438715a9b856
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706655"
---
# <a name="applyconditionallyc-operation"></a><span data-ttu-id="4962e-102">Applyconditionallyc-Vorgang</span><span class="sxs-lookup"><span data-stu-id="4962e-102">ApplyConditionallyC operation</span></span>

<span data-ttu-id="4962e-103">Namespace: [Microsoft. Quantum. Simulation. quantumprocessor. Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span><span class="sxs-lookup"><span data-stu-id="4962e-103">Namespace: [Microsoft.Quantum.Simulation.QuantumProcessor.Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span></span>

<span data-ttu-id="4962e-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="4962e-104">Package: [](https://nuget.org/packages/)</span></span>




```qsharp
operation ApplyConditionallyC<'T, 'U> (measurementResults : Result[], resultsValues : Result[], (onEqualOp : ('T => Unit is Ctl), equalArg : 'T), (onNonEqualOp : ('U => Unit is Ctl), nonEqualArg : 'U)) : Unit
```


## <a name="input"></a><span data-ttu-id="4962e-105">Eingabe</span><span class="sxs-lookup"><span data-stu-id="4962e-105">Input</span></span>

### <a name="measurementresults--__invalidresult__"></a><span data-ttu-id="4962e-106">"messrementresults": __ungültig <Result>__ []</span><span class="sxs-lookup"><span data-stu-id="4962e-106">measurementResults : __invalid<Result>__ []</span></span>




### <a name="resultsvalues--__invalidresult__"></a><span data-ttu-id="4962e-107">result values: __ungültig <Result>__ []</span><span class="sxs-lookup"><span data-stu-id="4962e-107">resultsValues : __invalid<Result>__ []</span></span>




### <a name="onequalop--t--unit-ctl"></a><span data-ttu-id="4962e-108">onequalop: 't => [Unit](xref:microsoft.quantum.lang-ref.unit) CTL</span><span class="sxs-lookup"><span data-stu-id="4962e-108">onEqualOp : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>




### <a name="equalarg--t"></a><span data-ttu-id="4962e-109">equalarg: 't</span><span class="sxs-lookup"><span data-stu-id="4962e-109">equalArg : 'T</span></span>




### <a name="onnonequalop--u--unit-ctl"></a><span data-ttu-id="4962e-110">onnonequalop: "U => [Unit](xref:microsoft.quantum.lang-ref.unit) CTL</span><span class="sxs-lookup"><span data-stu-id="4962e-110">onNonEqualOp : 'U => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>




### <a name="nonequalarg--u"></a><span data-ttu-id="4962e-111">nicht equalarg: "U</span><span class="sxs-lookup"><span data-stu-id="4962e-111">nonEqualArg : 'U</span></span>





## <a name="output--unit"></a><span data-ttu-id="4962e-112">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="4962e-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="4962e-113">Typparameter</span><span class="sxs-lookup"><span data-stu-id="4962e-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="4962e-114">GIF</span><span class="sxs-lookup"><span data-stu-id="4962e-114">'T</span></span>


### <a name="u"></a><span data-ttu-id="4962e-115">"U</span><span class="sxs-lookup"><span data-stu-id="4962e-115">'U</span></span>

