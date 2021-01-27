---
uid: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions.ApplyIfZeroCA
title: Applyif nuloca-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions
qsharp.name: ApplyIfZeroCA
qsharp.summary: ''
ms.openlocfilehash: f7dd30171acd3786c6d012b82b9abf99f9042caf
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98858266"
---
# <a name="applyifzeroca-operation"></a><span data-ttu-id="e01ff-102">Applyif nuloca-Vorgang</span><span class="sxs-lookup"><span data-stu-id="e01ff-102">ApplyIfZeroCA operation</span></span>

<span data-ttu-id="e01ff-103">Namespace: [Microsoft. Quantum. Simulation. quantumprocessor. Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span><span class="sxs-lookup"><span data-stu-id="e01ff-103">Namespace: [Microsoft.Quantum.Simulation.QuantumProcessor.Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span></span>

<span data-ttu-id="e01ff-104">Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="e01ff-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>




```qsharp
operation ApplyIfZeroCA<'T> (measurementResult : Result, (onResultZeroOp : ('T => Unit is Ctl + Adj), zeroArg : 'T)) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="e01ff-105">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e01ff-105">Input</span></span>

### <a name="measurementresult--__invalidresult__"></a><span data-ttu-id="e01ff-106">messrementresult: __ungültig <Result>__</span><span class="sxs-lookup"><span data-stu-id="e01ff-106">measurementResult : __invalid<Result>__</span></span>




### <a name="onresultzeroop--t--unit--is-adj--ctl"></a><span data-ttu-id="e01ff-107">onresultzeroop: 't => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="e01ff-107">onResultZeroOp : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>




### <a name="zeroarg--t"></a><span data-ttu-id="e01ff-108">NULL: nicht</span><span class="sxs-lookup"><span data-stu-id="e01ff-108">zeroArg : 'T</span></span>





## <a name="output--unit"></a><span data-ttu-id="e01ff-109">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="e01ff-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="e01ff-110">Typparameter</span><span class="sxs-lookup"><span data-stu-id="e01ff-110">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="e01ff-111">GIF</span><span class="sxs-lookup"><span data-stu-id="e01ff-111">'T</span></span>

