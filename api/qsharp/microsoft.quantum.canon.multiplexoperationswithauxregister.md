---
uid: Microsoft.Quantum.Canon.MultiplexOperationsWithAuxRegister
title: Multiplexoperationswithauxregister-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: MultiplexOperationsWithAuxRegister
qsharp.summary: Implementation step of MultiplexOperations.
ms.openlocfilehash: f6a90657324f8528aaa2e9e511a7f8cbcd2f540f
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703962"
---
# <a name="multiplexoperationswithauxregister-operation"></a><span data-ttu-id="99e2b-102">Multiplexoperationswithauxregister-Vorgang</span><span class="sxs-lookup"><span data-stu-id="99e2b-102">MultiplexOperationsWithAuxRegister operation</span></span>

<span data-ttu-id="99e2b-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="99e2b-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="99e2b-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="99e2b-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="99e2b-105">Implementierungs Schritt von multiplexoperations.</span><span class="sxs-lookup"><span data-stu-id="99e2b-105">Implementation step of MultiplexOperations.</span></span>

```qsharp
operation MultiplexOperationsWithAuxRegister<'T> (unitaries : ('T => Unit is Adj + Ctl)[], auxillaryRegister : Qubit[], index : Microsoft.Quantum.Arithmetic.LittleEndian, target : 'T) : Unit
```


## <a name="input"></a><span data-ttu-id="99e2b-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="99e2b-106">Input</span></span>

### <a name="unitaries--t--unit-adj--ctl"></a><span data-ttu-id="99e2b-107">Uni-Zuflüsse: 't => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL []</span><span class="sxs-lookup"><span data-stu-id="99e2b-107">unitaries : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl[]</span></span>




### <a name="auxillaryregister--qubit"></a><span data-ttu-id="99e2b-108">"auxillaryregister": [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="99e2b-108">auxillaryRegister : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>




### <a name="index--littleendian"></a><span data-ttu-id="99e2b-109">Index: [littleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="99e2b-109">index : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>




### <a name="target--t"></a><span data-ttu-id="99e2b-110">Ziel: 't</span><span class="sxs-lookup"><span data-stu-id="99e2b-110">target : 'T</span></span>





## <a name="output--unit"></a><span data-ttu-id="99e2b-111">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="99e2b-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="99e2b-112">Typparameter</span><span class="sxs-lookup"><span data-stu-id="99e2b-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="99e2b-113">GIF</span><span class="sxs-lookup"><span data-stu-id="99e2b-113">'T</span></span>



## <a name="see-also"></a><span data-ttu-id="99e2b-114">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="99e2b-114">See Also</span></span>

- [<span data-ttu-id="99e2b-115">Microsoft. Quantum. Canon. multiplexoperations</span><span class="sxs-lookup"><span data-stu-id="99e2b-115">Microsoft.Quantum.Canon.MultiplexOperations</span></span>](xref:Microsoft.Quantum.Canon.MultiplexOperations)