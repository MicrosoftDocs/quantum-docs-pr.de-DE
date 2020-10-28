---
uid: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions.ApplyConditionally
title: Applybedingt-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions
qsharp.name: ApplyConditionally
qsharp.summary: ''
ms.openlocfilehash: fe623b240e35ee88f673b6e90db6307ef701d049
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92701711"
---
# <a name="applyconditionally-operation"></a><span data-ttu-id="ca1ea-102">Applybedingt-Vorgang</span><span class="sxs-lookup"><span data-stu-id="ca1ea-102">ApplyConditionally operation</span></span>

<span data-ttu-id="ca1ea-103">Namespace: [Microsoft. Quantum. Simulation. quantumprocessor. Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span><span class="sxs-lookup"><span data-stu-id="ca1ea-103">Namespace: [Microsoft.Quantum.Simulation.QuantumProcessor.Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span></span>

<span data-ttu-id="ca1ea-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="ca1ea-104">Package: [](https://nuget.org/packages/)</span></span>




```qsharp
operation ApplyConditionally<'T, 'U> (measurementResults : Result[], resultsValues : Result[], (onEqualOp : ('T => Unit), equalArg : 'T), (onNonEqualOp : ('U => Unit), nonEqualArg : 'U)) : Unit
```


## <a name="input"></a><span data-ttu-id="ca1ea-105">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ca1ea-105">Input</span></span>

### <a name="measurementresults--__invalidresult__"></a><span data-ttu-id="ca1ea-106">"messrementresults": __ungültig <Result>__ []</span><span class="sxs-lookup"><span data-stu-id="ca1ea-106">measurementResults : __invalid<Result>__ []</span></span>




### <a name="resultsvalues--__invalidresult__"></a><span data-ttu-id="ca1ea-107">result values: __ungültig <Result>__ []</span><span class="sxs-lookup"><span data-stu-id="ca1ea-107">resultsValues : __invalid<Result>__ []</span></span>




### <a name="onequalop--t--unit"></a><span data-ttu-id="ca1ea-108">onequalop: 't => [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="ca1ea-108">onEqualOp : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 




### <a name="equalarg--t"></a><span data-ttu-id="ca1ea-109">equalarg: 't</span><span class="sxs-lookup"><span data-stu-id="ca1ea-109">equalArg : 'T</span></span>




### <a name="onnonequalop--u--unit"></a><span data-ttu-id="ca1ea-110">onnonequalop: ' U => [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="ca1ea-110">onNonEqualOp : 'U => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 




### <a name="nonequalarg--u"></a><span data-ttu-id="ca1ea-111">nicht equalarg: "U</span><span class="sxs-lookup"><span data-stu-id="ca1ea-111">nonEqualArg : 'U</span></span>





## <a name="output--unit"></a><span data-ttu-id="ca1ea-112">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="ca1ea-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="ca1ea-113">Typparameter</span><span class="sxs-lookup"><span data-stu-id="ca1ea-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="ca1ea-114">GIF</span><span class="sxs-lookup"><span data-stu-id="ca1ea-114">'T</span></span>


### <a name="u"></a><span data-ttu-id="ca1ea-115">"U</span><span class="sxs-lookup"><span data-stu-id="ca1ea-115">'U</span></span>

