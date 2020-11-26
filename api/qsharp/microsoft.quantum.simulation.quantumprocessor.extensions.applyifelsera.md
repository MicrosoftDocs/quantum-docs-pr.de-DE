---
uid: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions.ApplyIfElseRA
title: Applyifelsera-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions
qsharp.name: ApplyIfElseRA
qsharp.summary: ''
ms.openlocfilehash: 48819440bf0d55f9a44ca8f76927692d48925e50
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96192705"
---
# <a name="applyifelsera-operation"></a><span data-ttu-id="6d4cd-102">Applyifelsera-Vorgang</span><span class="sxs-lookup"><span data-stu-id="6d4cd-102">ApplyIfElseRA operation</span></span>

<span data-ttu-id="6d4cd-103">Namespace: [Microsoft. Quantum. Simulation. quantumprocessor. Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span><span class="sxs-lookup"><span data-stu-id="6d4cd-103">Namespace: [Microsoft.Quantum.Simulation.QuantumProcessor.Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span></span>

<span data-ttu-id="6d4cd-104">Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="6d4cd-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>




```qsharp
operation ApplyIfElseRA<'T, 'U> (measurementResult : Result, (onResultZeroOp : ('T => Unit is Adj), zeroArg : 'T), (onResultOneOp : ('U => Unit is Adj), oneArg : 'U)) : Unit is Adj
```


## <a name="input"></a><span data-ttu-id="6d4cd-105">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6d4cd-105">Input</span></span>

### <a name="measurementresult--__invalidresult__"></a><span data-ttu-id="6d4cd-106">messrementresult: __ungültig <Result>__</span><span class="sxs-lookup"><span data-stu-id="6d4cd-106">measurementResult : __invalid<Result>__</span></span>




### <a name="onresultzeroop--t--unit--is-adj"></a><span data-ttu-id="6d4cd-107">onresultzeroop: 't => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ</span><span class="sxs-lookup"><span data-stu-id="6d4cd-107">onResultZeroOp : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>




### <a name="zeroarg--t"></a><span data-ttu-id="6d4cd-108">NULL: nicht</span><span class="sxs-lookup"><span data-stu-id="6d4cd-108">zeroArg : 'T</span></span>




### <a name="onresultoneop--u--unit--is-adj"></a><span data-ttu-id="6d4cd-109">onresultoneop: "U => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ</span><span class="sxs-lookup"><span data-stu-id="6d4cd-109">onResultOneOp : 'U => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>




### <a name="onearg--u"></a><span data-ttu-id="6d4cd-110">onearg: "U</span><span class="sxs-lookup"><span data-stu-id="6d4cd-110">oneArg : 'U</span></span>





## <a name="output--unit"></a><span data-ttu-id="6d4cd-111">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="6d4cd-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="6d4cd-112">Typparameter</span><span class="sxs-lookup"><span data-stu-id="6d4cd-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="6d4cd-113">GIF</span><span class="sxs-lookup"><span data-stu-id="6d4cd-113">'T</span></span>


### <a name="u"></a><span data-ttu-id="6d4cd-114">"U</span><span class="sxs-lookup"><span data-stu-id="6d4cd-114">'U</span></span>

