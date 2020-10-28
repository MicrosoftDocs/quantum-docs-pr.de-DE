---
uid: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions.ApplyConditionallyA
title: Applyconditionallya-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions
qsharp.name: ApplyConditionallyA
qsharp.summary: ''
ms.openlocfilehash: b6f7e7d6d51e531b0ec9e7e4f2f5772038421933
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92701706"
---
# <a name="applyconditionallya-operation"></a><span data-ttu-id="32342-102">Applyconditionallya-Vorgang</span><span class="sxs-lookup"><span data-stu-id="32342-102">ApplyConditionallyA operation</span></span>

<span data-ttu-id="32342-103">Namespace: [Microsoft. Quantum. Simulation. quantumprocessor. Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span><span class="sxs-lookup"><span data-stu-id="32342-103">Namespace: [Microsoft.Quantum.Simulation.QuantumProcessor.Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span></span>

<span data-ttu-id="32342-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="32342-104">Package: [](https://nuget.org/packages/)</span></span>




```qsharp
operation ApplyConditionallyA<'T, 'U> (measurementResults : Result[], resultsValues : Result[], (onEqualOp : ('T => Unit is Adj), equalArg : 'T), (onNonEqualOp : ('U => Unit is Adj), nonEqualArg : 'U)) : Unit
```


## <a name="input"></a><span data-ttu-id="32342-105">Eingabe</span><span class="sxs-lookup"><span data-stu-id="32342-105">Input</span></span>

### <a name="measurementresults--__invalidresult__"></a><span data-ttu-id="32342-106">"messrementresults": __ungültig <Result>__ []</span><span class="sxs-lookup"><span data-stu-id="32342-106">measurementResults : __invalid<Result>__ []</span></span>




### <a name="resultsvalues--__invalidresult__"></a><span data-ttu-id="32342-107">result values: __ungültig <Result>__ []</span><span class="sxs-lookup"><span data-stu-id="32342-107">resultsValues : __invalid<Result>__ []</span></span>




### <a name="onequalop--t--unit-adj"></a><span data-ttu-id="32342-108">onequalop: 't => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ</span><span class="sxs-lookup"><span data-stu-id="32342-108">onEqualOp : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>




### <a name="equalarg--t"></a><span data-ttu-id="32342-109">equalarg: 't</span><span class="sxs-lookup"><span data-stu-id="32342-109">equalArg : 'T</span></span>




### <a name="onnonequalop--u--unit-adj"></a><span data-ttu-id="32342-110">onnonequalop: "U => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ</span><span class="sxs-lookup"><span data-stu-id="32342-110">onNonEqualOp : 'U => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>




### <a name="nonequalarg--u"></a><span data-ttu-id="32342-111">nicht equalarg: "U</span><span class="sxs-lookup"><span data-stu-id="32342-111">nonEqualArg : 'U</span></span>





## <a name="output--unit"></a><span data-ttu-id="32342-112">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="32342-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="32342-113">Typparameter</span><span class="sxs-lookup"><span data-stu-id="32342-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="32342-114">GIF</span><span class="sxs-lookup"><span data-stu-id="32342-114">'T</span></span>


### <a name="u"></a><span data-ttu-id="32342-115">"U</span><span class="sxs-lookup"><span data-stu-id="32342-115">'U</span></span>

