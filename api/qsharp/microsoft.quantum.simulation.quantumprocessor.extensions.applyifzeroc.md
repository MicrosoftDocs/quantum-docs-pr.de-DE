---
uid: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions.ApplyIfZeroC
title: Applyif zeroc-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions
qsharp.name: ApplyIfZeroC
qsharp.summary: ''
ms.openlocfilehash: c4d1618ff5e2a3d61823eddd6905445effcecfdd
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854189"
---
# <a name="applyifzeroc-operation"></a><span data-ttu-id="bbd61-102">Applyif zeroc-Vorgang</span><span class="sxs-lookup"><span data-stu-id="bbd61-102">ApplyIfZeroC operation</span></span>

<span data-ttu-id="bbd61-103">Namespace: [Microsoft. Quantum. Simulation. quantumprocessor. Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span><span class="sxs-lookup"><span data-stu-id="bbd61-103">Namespace: [Microsoft.Quantum.Simulation.QuantumProcessor.Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span></span>

<span data-ttu-id="bbd61-104">Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="bbd61-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>




```qsharp
operation ApplyIfZeroC<'T> (measurementResult : Result, (onResultZeroOp : ('T => Unit is Ctl), zeroArg : 'T)) : Unit is Ctl
```


## <a name="input"></a><span data-ttu-id="bbd61-105">Eingabe</span><span class="sxs-lookup"><span data-stu-id="bbd61-105">Input</span></span>

### <a name="measurementresult--__invalidresult__"></a><span data-ttu-id="bbd61-106">messrementresult: __ungültig <Result>__</span><span class="sxs-lookup"><span data-stu-id="bbd61-106">measurementResult : __invalid<Result>__</span></span>




### <a name="onresultzeroop--t--unit--is-ctl"></a><span data-ttu-id="bbd61-107">onresultzeroop: 't => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist CTL</span><span class="sxs-lookup"><span data-stu-id="bbd61-107">onResultZeroOp : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>




### <a name="zeroarg--t"></a><span data-ttu-id="bbd61-108">NULL: nicht</span><span class="sxs-lookup"><span data-stu-id="bbd61-108">zeroArg : 'T</span></span>





## <a name="output--unit"></a><span data-ttu-id="bbd61-109">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="bbd61-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="bbd61-110">Typparameter</span><span class="sxs-lookup"><span data-stu-id="bbd61-110">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="bbd61-111">GIF</span><span class="sxs-lookup"><span data-stu-id="bbd61-111">'T</span></span>

