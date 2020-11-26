---
uid: Microsoft.Quantum.ErrorCorrection.ApplyBitFlipEncoder
title: Applybitflipcoder-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: ApplyBitFlipEncoder
qsharp.summary: >-
  Private operation used to implement both the bit flip encoder and decoder.

  Note that this encoder can make use of in-place coherent recovery, in which case it will "cause" the error described by the initial state of `auxQubits`. In particular, if `auxQubits` are initially in the state $\ket{10}$, this will cause an $X_1$ error on the encoded qubit.
ms.openlocfilehash: e56e84effa001f104bbd5e28e7181dbd39a4cf5e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96201290"
---
# <a name="applybitflipencoder-operation"></a><span data-ttu-id="66105-102">Applybitflipcoder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="66105-102">ApplyBitFlipEncoder operation</span></span>

<span data-ttu-id="66105-103">Namespace: [Microsoft. Quantum. errorcorrection](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="66105-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="66105-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="66105-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="66105-105">Der private Vorgang, der verwendet wird, um den bitflip-Encoder und den Decoder zu implementieren</span><span class="sxs-lookup"><span data-stu-id="66105-105">Private operation used to implement both the bit flip encoder and decoder.</span></span>

<span data-ttu-id="66105-106">Beachten Sie, dass dieser Encoder eine direkte, kohärente Wiederherstellung verwenden kann. in diesem Fall wird der Fehler, der durch den ursprünglichen Zustand von beschrieben wird, "verursacht" `auxQubits` .</span><span class="sxs-lookup"><span data-stu-id="66105-106">Note that this encoder can make use of in-place coherent recovery, in which case it will "cause" the error described by the initial state of `auxQubits`.</span></span>
<span data-ttu-id="66105-107">Insbesondere, wenn `auxQubits` sich anfänglich im Status $ \ket {10} $ befindet, führt dies zu einem $X _1 $ Error für das codierte Qubit.</span><span class="sxs-lookup"><span data-stu-id="66105-107">In particular, if `auxQubits` are initially in the state $\ket{10}$, this will cause an $X_1$ error on the encoded qubit.</span></span>

```qsharp
operation ApplyBitFlipEncoder (coherentRecovery : Bool, data : Qubit[], scratch : Qubit[]) : Unit is Adj
```


## <a name="input"></a><span data-ttu-id="66105-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="66105-108">Input</span></span>

### <a name="coherentrecovery--bool"></a><span data-ttu-id="66105-109">Coherent Recovery: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="66105-109">coherentRecovery : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>




### <a name="data--qubit"></a><span data-ttu-id="66105-110">Daten: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="66105-110">data : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>




### <a name="scratch--qubit"></a><span data-ttu-id="66105-111">Scratch: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="66105-111">scratch : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>





## <a name="output--unit"></a><span data-ttu-id="66105-112">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="66105-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="references"></a><span data-ttu-id="66105-113">Referenzen</span><span class="sxs-lookup"><span data-stu-id="66105-113">References</span></span>

- <span data-ttu-id="66105-114">doi: 10.1103/physreva. 85.044302</span><span class="sxs-lookup"><span data-stu-id="66105-114">doi:10.1103/PhysRevA.85.044302</span></span>