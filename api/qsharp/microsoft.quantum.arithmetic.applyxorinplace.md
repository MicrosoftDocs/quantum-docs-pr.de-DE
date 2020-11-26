---
uid: Microsoft.Quantum.Arithmetic.ApplyXorInPlace
title: Applyxorinplace-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyXorInPlace
qsharp.summary: Applies a bitwise-XOR operation between a classical integer and an integer represented by a register of qubits.
ms.openlocfilehash: b7fc20ac421d5cff9baa3fe05450c1564f123505
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96210112"
---
# <a name="applyxorinplace-operation"></a><span data-ttu-id="43606-102">Applyxorinplace-Vorgang</span><span class="sxs-lookup"><span data-stu-id="43606-102">ApplyXorInPlace operation</span></span>

<span data-ttu-id="43606-103">Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="43606-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="43606-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="43606-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="43606-105">Wendet eine bitweise XOR-Operation zwischen einer klassischen Ganzzahl und einer ganzen Zahl an, die durch ein Register von Qubits dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="43606-105">Applies a bitwise-XOR operation between a classical integer and an integer represented by a register of qubits.</span></span>

```qsharp
operation ApplyXorInPlace (value : Int, target : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="43606-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="43606-106">Description</span></span>

<span data-ttu-id="43606-107">Wendet `X` Vorgänge auf Qubits in einem Little-d-Register auf der Grundlage von 1 Bits in einer ganzen Zahl an.</span><span class="sxs-lookup"><span data-stu-id="43606-107">Applies `X` operations to qubits in a little-endian register based on 1 bits in an integer.</span></span>

<span data-ttu-id="43606-108">`value`Beachten Sie, dass eine ganze Zahl ohne Vorzeichen ist, die in codiert ist, und führen Sie `target` dann `InPlaceXorLE` einen von der folgenden Zuordnung angegebenen Vorgang aus: $ \ket{y}\rightarrow \ket{y\oplus a} $, wobei $ \oplus $ der bitweise exklusive OR-Operator ist.</span><span class="sxs-lookup"><span data-stu-id="43606-108">Let us denote `value` by a and let y be an unsigned integer encoded in `target`, then `InPlaceXorLE` performs an operation given by the following map: $\ket{y}\rightarrow \ket{y\oplus a}$ , where $\oplus$ is the bitwise exclusive OR operator.</span></span>

## <a name="input"></a><span data-ttu-id="43606-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="43606-109">Input</span></span>

### <a name="value--int"></a><span data-ttu-id="43606-110">Wert: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="43606-110">value : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="43606-111">Eine Ganzzahl, bei der angenommen wird, dass Sie nicht negativ ist.</span><span class="sxs-lookup"><span data-stu-id="43606-111">An integer which is assumed to be non-negative.</span></span>


### <a name="target--littleendian"></a><span data-ttu-id="43606-112">Ziel: [littleenddian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="43606-112">target : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="43606-113">Ein Quantum-Register, das zum Speichern von `value` in Little-d-Codierungen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="43606-113">A quantum register which is used to store `value` in little-endian encoding.</span></span>



## <a name="output--unit"></a><span data-ttu-id="43606-114">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="43606-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

