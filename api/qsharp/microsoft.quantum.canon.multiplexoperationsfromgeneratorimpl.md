---
uid: Microsoft.Quantum.Canon.MultiplexOperationsFromGeneratorImpl
title: Multiplexoperationsfromgeneratorimpl-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: MultiplexOperationsFromGeneratorImpl
qsharp.summary: Implementation step of `MultiplexOperationsFromGenerator`.
ms.openlocfilehash: 98ba9cd24f04b8417cb176ee1630402483bc3b52
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96206050"
---
# <a name="multiplexoperationsfromgeneratorimpl-operation"></a><span data-ttu-id="a1c55-102">Multiplexoperationsfromgeneratorimpl-Vorgang</span><span class="sxs-lookup"><span data-stu-id="a1c55-102">MultiplexOperationsFromGeneratorImpl operation</span></span>

<span data-ttu-id="a1c55-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="a1c55-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="a1c55-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a1c55-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="a1c55-105">Implementierungs Schritt von `MultiplexOperationsFromGenerator` .</span><span class="sxs-lookup"><span data-stu-id="a1c55-105">Implementation step of `MultiplexOperationsFromGenerator`.</span></span>

```qsharp
operation MultiplexOperationsFromGeneratorImpl<'T> (unitaryGenerator : (Int, Int, (Int -> ('T => Unit is Adj + Ctl))), auxiliary : Qubit[], index : Microsoft.Quantum.Arithmetic.LittleEndian, target : 'T) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="a1c55-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a1c55-106">Input</span></span>

### <a name="unitarygenerator--intintint---t--unit--is-adj--ctl"></a><span data-ttu-id="a1c55-107">unitarygenerator: ([int](xref:microsoft.quantum.lang-ref.int),[int](xref:microsoft.quantum.lang-ref.int),[int](xref:microsoft.quantum.lang-ref.int) -> 't => [Unit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL)</span><span class="sxs-lookup"><span data-stu-id="a1c55-107">unitaryGenerator : ([Int](xref:microsoft.quantum.lang-ref.int),[Int](xref:microsoft.quantum.lang-ref.int),[Int](xref:microsoft.quantum.lang-ref.int) -> 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl)</span></span>




### <a name="auxiliary--qubit"></a><span data-ttu-id="a1c55-108">Zusatz: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="a1c55-108">auxiliary : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>




### <a name="index--littleendian"></a><span data-ttu-id="a1c55-109">Index: [littleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="a1c55-109">index : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>




### <a name="target--t"></a><span data-ttu-id="a1c55-110">Ziel: 't</span><span class="sxs-lookup"><span data-stu-id="a1c55-110">target : 'T</span></span>





## <a name="output--unit"></a><span data-ttu-id="a1c55-111">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="a1c55-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="a1c55-112">Typparameter</span><span class="sxs-lookup"><span data-stu-id="a1c55-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="a1c55-113">GIF</span><span class="sxs-lookup"><span data-stu-id="a1c55-113">'T</span></span>



## <a name="see-also"></a><span data-ttu-id="a1c55-114">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="a1c55-114">See Also</span></span>

- [<span data-ttu-id="a1c55-115">Microsoft. Quantum. Canon. multiplexoperationsfromgenerator</span><span class="sxs-lookup"><span data-stu-id="a1c55-115">Microsoft.Quantum.Canon.MultiplexOperationsFromGenerator</span></span>](xref:Microsoft.Quantum.Canon.MultiplexOperationsFromGenerator)