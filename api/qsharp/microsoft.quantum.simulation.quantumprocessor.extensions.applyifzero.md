---
uid: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions.ApplyIfZero
title: Applyif Zero-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions
qsharp.name: ApplyIfZero
qsharp.summary: ''
ms.openlocfilehash: 867e2e78ea787c2376fb2b1dcc6c72694fe08621
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96230904"
---
# <a name="applyifzero-operation"></a><span data-ttu-id="20bab-102">Applyif Zero-Vorgang</span><span class="sxs-lookup"><span data-stu-id="20bab-102">ApplyIfZero operation</span></span>

<span data-ttu-id="20bab-103">Namespace: [Microsoft. Quantum. Simulation. quantumprocessor. Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span><span class="sxs-lookup"><span data-stu-id="20bab-103">Namespace: [Microsoft.Quantum.Simulation.QuantumProcessor.Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span></span>

<span data-ttu-id="20bab-104">Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="20bab-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>




```qsharp
operation ApplyIfZero<'T> (measurementResult : Result, (onResultZeroOp : ('T => Unit), zeroArg : 'T)) : Unit
```


## <a name="input"></a><span data-ttu-id="20bab-105">Eingabe</span><span class="sxs-lookup"><span data-stu-id="20bab-105">Input</span></span>

### <a name="measurementresult--__invalidresult__"></a><span data-ttu-id="20bab-106">messrementresult: __ungültig <Result>__</span><span class="sxs-lookup"><span data-stu-id="20bab-106">measurementResult : __invalid<Result>__</span></span>




### <a name="onresultzeroop--t--unit"></a><span data-ttu-id="20bab-107">onresultzeroop: 't => [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="20bab-107">onResultZeroOp : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 




### <a name="zeroarg--t"></a><span data-ttu-id="20bab-108">NULL: nicht</span><span class="sxs-lookup"><span data-stu-id="20bab-108">zeroArg : 'T</span></span>





## <a name="output--unit"></a><span data-ttu-id="20bab-109">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="20bab-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="20bab-110">Typparameter</span><span class="sxs-lookup"><span data-stu-id="20bab-110">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="20bab-111">GIF</span><span class="sxs-lookup"><span data-stu-id="20bab-111">'T</span></span>

