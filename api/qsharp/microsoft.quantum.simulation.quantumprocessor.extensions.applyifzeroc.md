---
uid: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions.ApplyIfZeroC
title: Applyif zeroc-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions
qsharp.name: ApplyIfZeroC
qsharp.summary: ''
ms.openlocfilehash: 9a73ea9ec607bec89c996c096b235a72185b453d
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96230836"
---
# <a name="applyifzeroc-operation"></a><span data-ttu-id="1e432-102">Applyif zeroc-Vorgang</span><span class="sxs-lookup"><span data-stu-id="1e432-102">ApplyIfZeroC operation</span></span>

<span data-ttu-id="1e432-103">Namespace: [Microsoft. Quantum. Simulation. quantumprocessor. Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span><span class="sxs-lookup"><span data-stu-id="1e432-103">Namespace: [Microsoft.Quantum.Simulation.QuantumProcessor.Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span></span>

<span data-ttu-id="1e432-104">Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="1e432-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>




```qsharp
operation ApplyIfZeroC<'T> (measurementResult : Result, (onResultZeroOp : ('T => Unit is Ctl), zeroArg : 'T)) : Unit is Ctl
```


## <a name="input"></a><span data-ttu-id="1e432-105">Eingabe</span><span class="sxs-lookup"><span data-stu-id="1e432-105">Input</span></span>

### <a name="measurementresult--__invalidresult__"></a><span data-ttu-id="1e432-106">messrementresult: __ungültig <Result>__</span><span class="sxs-lookup"><span data-stu-id="1e432-106">measurementResult : __invalid<Result>__</span></span>




### <a name="onresultzeroop--t--unit--is-ctl"></a><span data-ttu-id="1e432-107">onresultzeroop: 't => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist CTL</span><span class="sxs-lookup"><span data-stu-id="1e432-107">onResultZeroOp : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>




### <a name="zeroarg--t"></a><span data-ttu-id="1e432-108">NULL: nicht</span><span class="sxs-lookup"><span data-stu-id="1e432-108">zeroArg : 'T</span></span>





## <a name="output--unit"></a><span data-ttu-id="1e432-109">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="1e432-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="1e432-110">Typparameter</span><span class="sxs-lookup"><span data-stu-id="1e432-110">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="1e432-111">GIF</span><span class="sxs-lookup"><span data-stu-id="1e432-111">'T</span></span>

