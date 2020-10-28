---
uid: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions.ApplyIfElseR
title: Applyifelser-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions
qsharp.name: ApplyIfElseR
qsharp.summary: ''
ms.openlocfilehash: ca9db334bb62e043933f99e405612957831efdcb
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92724768"
---
# <a name="applyifelser-operation"></a><span data-ttu-id="5fec4-102">Applyifelser-Vorgang</span><span class="sxs-lookup"><span data-stu-id="5fec4-102">ApplyIfElseR operation</span></span>

<span data-ttu-id="5fec4-103">Namespace: [Microsoft. Quantum. Simulation. quantumprocessor. Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span><span class="sxs-lookup"><span data-stu-id="5fec4-103">Namespace: [Microsoft.Quantum.Simulation.QuantumProcessor.Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span></span>

<span data-ttu-id="5fec4-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="5fec4-104">Package: [](https://nuget.org/packages/)</span></span>




```qsharp
operation ApplyIfElseR<'T, 'U> (measurementResult : Result, (onResultZeroOp : ('T => Unit), zeroArg : 'T), (onResultOneOp : ('U => Unit), oneArg : 'U)) : Unit
```


## <a name="input"></a><span data-ttu-id="5fec4-105">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5fec4-105">Input</span></span>

### <a name="measurementresult--__invalidresult__"></a><span data-ttu-id="5fec4-106">messrementresult: __ungültig <Result>__</span><span class="sxs-lookup"><span data-stu-id="5fec4-106">measurementResult : __invalid<Result>__</span></span>




### <a name="onresultzeroop--t--unit"></a><span data-ttu-id="5fec4-107">onresultzeroop: 't => [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="5fec4-107">onResultZeroOp : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 




### <a name="zeroarg--t"></a><span data-ttu-id="5fec4-108">NULL: nicht</span><span class="sxs-lookup"><span data-stu-id="5fec4-108">zeroArg : 'T</span></span>




### <a name="onresultoneop--u--unit"></a><span data-ttu-id="5fec4-109">onresultoneop: ' U => [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="5fec4-109">onResultOneOp : 'U => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 




### <a name="onearg--u"></a><span data-ttu-id="5fec4-110">onearg: "U</span><span class="sxs-lookup"><span data-stu-id="5fec4-110">oneArg : 'U</span></span>





## <a name="output--unit"></a><span data-ttu-id="5fec4-111">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="5fec4-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="5fec4-112">Typparameter</span><span class="sxs-lookup"><span data-stu-id="5fec4-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="5fec4-113">GIF</span><span class="sxs-lookup"><span data-stu-id="5fec4-113">'T</span></span>


### <a name="u"></a><span data-ttu-id="5fec4-114">"U</span><span class="sxs-lookup"><span data-stu-id="5fec4-114">'U</span></span>

