---
uid: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions.ApplyIfZeroA
title: Applyif zeroa-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions
qsharp.name: ApplyIfZeroA
qsharp.summary: ''
ms.openlocfilehash: 124c5bbabc9e22804734ddbde955312db9655187
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92725705"
---
# <a name="applyifzeroa-operation"></a><span data-ttu-id="56297-102">Applyif zeroa-Vorgang</span><span class="sxs-lookup"><span data-stu-id="56297-102">ApplyIfZeroA operation</span></span>

<span data-ttu-id="56297-103">Namespace: [Microsoft. Quantum. Simulation. quantumprocessor. Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span><span class="sxs-lookup"><span data-stu-id="56297-103">Namespace: [Microsoft.Quantum.Simulation.QuantumProcessor.Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span></span>

<span data-ttu-id="56297-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="56297-104">Package: [](https://nuget.org/packages/)</span></span>




```qsharp
operation ApplyIfZeroA<'T> (measurementResult : Result, (onResultZeroOp : ('T => Unit is Adj), zeroArg : 'T)) : Unit
```


## <a name="input"></a><span data-ttu-id="56297-105">Eingabe</span><span class="sxs-lookup"><span data-stu-id="56297-105">Input</span></span>

### <a name="measurementresult--__invalidresult__"></a><span data-ttu-id="56297-106">messrementresult: __ungültig <Result>__</span><span class="sxs-lookup"><span data-stu-id="56297-106">measurementResult : __invalid<Result>__</span></span>




### <a name="onresultzeroop--t--unit-adj"></a><span data-ttu-id="56297-107">onresultzeroop: 't => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ</span><span class="sxs-lookup"><span data-stu-id="56297-107">onResultZeroOp : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>




### <a name="zeroarg--t"></a><span data-ttu-id="56297-108">NULL: nicht</span><span class="sxs-lookup"><span data-stu-id="56297-108">zeroArg : 'T</span></span>





## <a name="output--unit"></a><span data-ttu-id="56297-109">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="56297-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="56297-110">Typparameter</span><span class="sxs-lookup"><span data-stu-id="56297-110">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="56297-111">GIF</span><span class="sxs-lookup"><span data-stu-id="56297-111">'T</span></span>

