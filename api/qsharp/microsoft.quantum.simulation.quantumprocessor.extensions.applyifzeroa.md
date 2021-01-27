---
uid: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions.ApplyIfZeroA
title: Applyif zeroa-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions
qsharp.name: ApplyIfZeroA
qsharp.summary: ''
ms.openlocfilehash: 812b7a830d963b4bb73c32ba1c136e506789e997
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854199"
---
# <a name="applyifzeroa-operation"></a><span data-ttu-id="c138a-102">Applyif zeroa-Vorgang</span><span class="sxs-lookup"><span data-stu-id="c138a-102">ApplyIfZeroA operation</span></span>

<span data-ttu-id="c138a-103">Namespace: [Microsoft. Quantum. Simulation. quantumprocessor. Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span><span class="sxs-lookup"><span data-stu-id="c138a-103">Namespace: [Microsoft.Quantum.Simulation.QuantumProcessor.Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span></span>

<span data-ttu-id="c138a-104">Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="c138a-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>




```qsharp
operation ApplyIfZeroA<'T> (measurementResult : Result, (onResultZeroOp : ('T => Unit is Adj), zeroArg : 'T)) : Unit is Adj
```


## <a name="input"></a><span data-ttu-id="c138a-105">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c138a-105">Input</span></span>

### <a name="measurementresult--__invalidresult__"></a><span data-ttu-id="c138a-106">messrementresult: __ungültig <Result>__</span><span class="sxs-lookup"><span data-stu-id="c138a-106">measurementResult : __invalid<Result>__</span></span>




### <a name="onresultzeroop--t--unit--is-adj"></a><span data-ttu-id="c138a-107">onresultzeroop: 't => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ</span><span class="sxs-lookup"><span data-stu-id="c138a-107">onResultZeroOp : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>




### <a name="zeroarg--t"></a><span data-ttu-id="c138a-108">NULL: nicht</span><span class="sxs-lookup"><span data-stu-id="c138a-108">zeroArg : 'T</span></span>





## <a name="output--unit"></a><span data-ttu-id="c138a-109">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="c138a-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="c138a-110">Typparameter</span><span class="sxs-lookup"><span data-stu-id="c138a-110">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="c138a-111">GIF</span><span class="sxs-lookup"><span data-stu-id="c138a-111">'T</span></span>

