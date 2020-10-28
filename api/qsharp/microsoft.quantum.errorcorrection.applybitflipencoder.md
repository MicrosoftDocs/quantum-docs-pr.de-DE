---
uid: Microsoft.Quantum.ErrorCorrection.ApplyBitFlipEncoder
title: Applybitflipcoder-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: ApplyBitFlipEncoder
qsharp.summary: >-
  Private operation used to implement both the bit flip encoder and decoder.

  Note that this encoder can make use of in-place coherent recovery, in which case it will "cause" the error described by the initial state of `auxQubits`. In particular, if `auxQubits` are initially in the state $\ket{10}$, this will cause an $X_1$ error on the encoded qubit.
ms.openlocfilehash: 4d78cbb5892aabc600321185641bbf217bd4d745
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702558"
---
# <a name="applybitflipencoder-operation"></a><span data-ttu-id="62724-102">Applybitflipcoder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="62724-102">ApplyBitFlipEncoder operation</span></span>

<span data-ttu-id="62724-103">Namespace: [Microsoft. Quantum. errorcorrection](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="62724-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="62724-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="62724-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="62724-105">Der private Vorgang, der verwendet wird, um den bitflip-Encoder und den Decoder zu implementieren</span><span class="sxs-lookup"><span data-stu-id="62724-105">Private operation used to implement both the bit flip encoder and decoder.</span></span>

<span data-ttu-id="62724-106">Beachten Sie, dass dieser Encoder eine direkte, kohärente Wiederherstellung verwenden kann. in diesem Fall wird der Fehler, der durch den ursprünglichen Zustand von beschrieben wird, "verursacht" `auxQubits` .</span><span class="sxs-lookup"><span data-stu-id="62724-106">Note that this encoder can make use of in-place coherent recovery, in which case it will "cause" the error described by the initial state of `auxQubits`.</span></span>
<span data-ttu-id="62724-107">Insbesondere, wenn `auxQubits` sich anfänglich im Status $ \ket {10} $ befindet, führt dies zu einem $X _1 $ Error für das codierte Qubit.</span><span class="sxs-lookup"><span data-stu-id="62724-107">In particular, if `auxQubits` are initially in the state $\ket{10}$, this will cause an $X_1$ error on the encoded qubit.</span></span>

```qsharp
operation ApplyBitFlipEncoder (coherentRecovery : Bool, data : Qubit[], scratch : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="62724-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="62724-108">Input</span></span>

### <a name="coherentrecovery--bool"></a><span data-ttu-id="62724-109">Coherent Recovery: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="62724-109">coherentRecovery : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>




### <a name="data--qubit"></a><span data-ttu-id="62724-110">Daten: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="62724-110">data : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>




### <a name="scratch--qubit"></a><span data-ttu-id="62724-111">Scratch: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="62724-111">scratch : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>





## <a name="output--unit"></a><span data-ttu-id="62724-112">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="62724-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="references"></a><span data-ttu-id="62724-113">Referenzen</span><span class="sxs-lookup"><span data-stu-id="62724-113">References</span></span>

- <span data-ttu-id="62724-114">doi: 10.1103/physreva. 85.044302</span><span class="sxs-lookup"><span data-stu-id="62724-114">doi:10.1103/PhysRevA.85.044302</span></span>