---
uid: Microsoft.Quantum.Arithmetic.Sum
title: Summierungsvorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: Sum
qsharp.summary: Implements a reversible sum gate. Given a carry-in bit encoded in qubit `carryIn` and two summand bits encoded in `summand1` and `summand2`, computes the bitwise xor of `carryIn`, `summand1` and `summand2` in the qubit `summand2`.
ms.openlocfilehash: 7758e29c9f08f4d05253defbe5a43a5316289522
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96221792"
---
# <a name="sum-operation"></a><span data-ttu-id="9ce22-102">Summierungsvorgang</span><span class="sxs-lookup"><span data-stu-id="9ce22-102">Sum operation</span></span>

<span data-ttu-id="9ce22-103">Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="9ce22-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="9ce22-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="9ce22-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="9ce22-105">Implementiert ein umkehrbares Summen Gate.</span><span class="sxs-lookup"><span data-stu-id="9ce22-105">Implements a reversible sum gate.</span></span> <span data-ttu-id="9ce22-106">`carryIn` `summand1` `summand2` Berechnet das bitweise XOR von `carryIn` `summand1` und `summand2` im Qubit, `summand2` Wenn ein in Qubit codiertes und zwei Summen in und codiert sind.</span><span class="sxs-lookup"><span data-stu-id="9ce22-106">Given a carry-in bit encoded in qubit `carryIn` and two summand bits encoded in `summand1` and `summand2`, computes the bitwise xor of `carryIn`, `summand1` and `summand2` in the qubit `summand2`.</span></span>

```qsharp
operation Sum (carryIn : Qubit, summand1 : Qubit, summand2 : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="9ce22-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="9ce22-107">Input</span></span>

### <a name="carryin--qubit"></a><span data-ttu-id="9ce22-108">Carryin: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="9ce22-108">carryIn : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="9ce22-109">Ein-in-Qubit.</span><span class="sxs-lookup"><span data-stu-id="9ce22-109">Carry-in qubit.</span></span>


### <a name="summand1--qubit"></a><span data-ttu-id="9ce22-110">summand1: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="9ce22-110">summand1 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="9ce22-111">Erstes Summen-und Qubit-Wert.</span><span class="sxs-lookup"><span data-stu-id="9ce22-111">First summand qubit.</span></span>


### <a name="summand2--qubit"></a><span data-ttu-id="9ce22-112">summand2: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="9ce22-112">summand2 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="9ce22-113">Zweites Summen-und Qubit-Wert, wird durch das untere Bit der Summe von `summand1` und ersetzt `summand2` .</span><span class="sxs-lookup"><span data-stu-id="9ce22-113">Second summand qubit, is replaced with the lower bit of the sum of `summand1` and `summand2`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="9ce22-114">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="9ce22-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="9ce22-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9ce22-115">Remarks</span></span>

<span data-ttu-id="9ce22-116">Im Gegensatz zum- `Carry` Vorgang berechnet dies nicht das-Ausgangsbit.</span><span class="sxs-lookup"><span data-stu-id="9ce22-116">In contrast to the `Carry` operation, this does not compute the carry-out bit.</span></span>