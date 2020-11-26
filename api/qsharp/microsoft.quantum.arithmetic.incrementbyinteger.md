---
uid: Microsoft.Quantum.Arithmetic.IncrementByInteger
title: Incrementbyinteger-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: IncrementByInteger
qsharp.summary: Increments an unsigned quantum register by a classical integer, using phase rotations.
ms.openlocfilehash: fa5e75e91206aa5f33233c8a54d6e9e7ac2950e3
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96222965"
---
# <a name="incrementbyinteger-operation"></a><span data-ttu-id="43a57-102">Incrementbyinteger-Vorgang</span><span class="sxs-lookup"><span data-stu-id="43a57-102">IncrementByInteger operation</span></span>

<span data-ttu-id="43a57-103">Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="43a57-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="43a57-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="43a57-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="43a57-105">Erhöht mithilfe von Phasen Drehungen ein unsigniertes Quantum-Register durch eine klassische Ganzzahl.</span><span class="sxs-lookup"><span data-stu-id="43a57-105">Increments an unsigned quantum register by a classical integer, using phase rotations.</span></span>

```qsharp
operation IncrementByInteger (increment : Int, target : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="43a57-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="43a57-106">Description</span></span>

<span data-ttu-id="43a57-107">Angenommen, das `target` codiert eine Ganzzahl ohne Vorzeichen $x $ in einer Little-in-codiercodierung und `increment` ist gleich $a $.</span><span class="sxs-lookup"><span data-stu-id="43a57-107">Suppose that `target` encodes an unsigned integer $x$ in a little-endian encoding and that `increment` is equal to $a$.</span></span>
<span data-ttu-id="43a57-108">Anschließend implementiert dieser Vorgang die einheitliche $ \ket{x} \mapsto \ket{x + a} $, wobei die Addition Modulo $2 ^ n $ ist, wobei $n = \texttt{length (Target!)} $.</span><span class="sxs-lookup"><span data-stu-id="43a57-108">Then, this operation implements the unitary $\ket{x} \mapsto \ket{x + a}$, where the addition is performed modulo $2^n$, where $n = \texttt{Length(target!)}$.</span></span>

## <a name="input"></a><span data-ttu-id="43a57-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="43a57-109">Input</span></span>

### <a name="increment--int"></a><span data-ttu-id="43a57-110">Inkrement: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="43a57-110">increment : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="43a57-111">Die ganze Zahl, um die die `target` inkrementiert wird.</span><span class="sxs-lookup"><span data-stu-id="43a57-111">The integer by which the `target` is incremented by.</span></span>


### <a name="target--littleendian"></a><span data-ttu-id="43a57-112">Ziel: [littleenddian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="43a57-112">target : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="43a57-113">Ein Quantum-Register codiert eine Ganzzahl ohne Vorzeichen unter Verwendung der Little-d-Codierung.</span><span class="sxs-lookup"><span data-stu-id="43a57-113">A quantum register encoding an unsigned integer using little-endian encoding.</span></span>



## <a name="output--unit"></a><span data-ttu-id="43a57-114">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="43a57-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

