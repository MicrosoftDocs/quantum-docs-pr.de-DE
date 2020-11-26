---
uid: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions.ApplyIfZeroA
title: Applyif zeroa-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions
qsharp.name: ApplyIfZeroA
qsharp.summary: ''
ms.openlocfilehash: d57f07beddc94d11a2143ba5d1fd975760260731
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96230870"
---
# <a name="applyifzeroa-operation"></a><span data-ttu-id="88f17-102">Applyif zeroa-Vorgang</span><span class="sxs-lookup"><span data-stu-id="88f17-102">ApplyIfZeroA operation</span></span>

<span data-ttu-id="88f17-103">Namespace: [Microsoft. Quantum. Simulation. quantumprocessor. Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span><span class="sxs-lookup"><span data-stu-id="88f17-103">Namespace: [Microsoft.Quantum.Simulation.QuantumProcessor.Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span></span>

<span data-ttu-id="88f17-104">Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="88f17-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>




```qsharp
operation ApplyIfZeroA<'T> (measurementResult : Result, (onResultZeroOp : ('T => Unit is Adj), zeroArg : 'T)) : Unit is Adj
```


## <a name="input"></a><span data-ttu-id="88f17-105">Eingabe</span><span class="sxs-lookup"><span data-stu-id="88f17-105">Input</span></span>

### <a name="measurementresult--__invalidresult__"></a><span data-ttu-id="88f17-106">messrementresult: __ungültig <Result>__</span><span class="sxs-lookup"><span data-stu-id="88f17-106">measurementResult : __invalid<Result>__</span></span>




### <a name="onresultzeroop--t--unit--is-adj"></a><span data-ttu-id="88f17-107">onresultzeroop: 't => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ</span><span class="sxs-lookup"><span data-stu-id="88f17-107">onResultZeroOp : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>




### <a name="zeroarg--t"></a><span data-ttu-id="88f17-108">NULL: nicht</span><span class="sxs-lookup"><span data-stu-id="88f17-108">zeroArg : 'T</span></span>





## <a name="output--unit"></a><span data-ttu-id="88f17-109">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="88f17-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="88f17-110">Typparameter</span><span class="sxs-lookup"><span data-stu-id="88f17-110">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="88f17-111">GIF</span><span class="sxs-lookup"><span data-stu-id="88f17-111">'T</span></span>

