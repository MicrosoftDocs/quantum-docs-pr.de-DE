---
uid: Microsoft.Quantum.Arithmetic.Carry
title: Carry-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: Carry
qsharp.summary: Implements a reversible carry gate. Given a carry-in bit encoded in qubit `carryIn` and two summand bits encoded in `summand1` and `summand2`, computes the bitwise xor of `carryIn`, `summand1` and `summand2` in the qubit `summand2` and the carry-out is xored to the qubit `carryOut`.
ms.openlocfilehash: 2b977151861fb01be7d7dbad6e0a7b803fded880
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707402"
---
# <a name="carry-operation"></a><span data-ttu-id="9263a-102">Carry-Vorgang</span><span class="sxs-lookup"><span data-stu-id="9263a-102">Carry operation</span></span>

<span data-ttu-id="9263a-103">Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="9263a-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="9263a-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="9263a-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="9263a-105">Implementiert ein umkehrbares durchführen.</span><span class="sxs-lookup"><span data-stu-id="9263a-105">Implements a reversible carry gate.</span></span> <span data-ttu-id="9263a-106">Wenn ein in Qubit codiertes `carryIn` und zwei Summen in und codiert `summand1` `summand2` sind, berechnet das bitweise XOR von `carryIn` `summand1` und `summand2` im Qubit, `summand2` und die Überführung wird im Qubit-Element als XoReD `carryOut` festgestellt.</span><span class="sxs-lookup"><span data-stu-id="9263a-106">Given a carry-in bit encoded in qubit `carryIn` and two summand bits encoded in `summand1` and `summand2`, computes the bitwise xor of `carryIn`, `summand1` and `summand2` in the qubit `summand2` and the carry-out is xored to the qubit `carryOut`.</span></span>

```qsharp
operation Carry (carryIn : Qubit, summand1 : Qubit, summand2 : Qubit, carryOut : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="9263a-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="9263a-107">Input</span></span>

### <a name="carryin--qubit"></a><span data-ttu-id="9263a-108">Carryin: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="9263a-108">carryIn : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="9263a-109">Ein-in-Qubit.</span><span class="sxs-lookup"><span data-stu-id="9263a-109">Carry-in qubit.</span></span>


### <a name="summand1--qubit"></a><span data-ttu-id="9263a-110">summand1: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="9263a-110">summand1 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="9263a-111">Erstes Summen-und Qubit-Wert.</span><span class="sxs-lookup"><span data-stu-id="9263a-111">First summand qubit.</span></span>


### <a name="summand2--qubit"></a><span data-ttu-id="9263a-112">summand2: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="9263a-112">summand2 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="9263a-113">Zweites Summen-und Qubit-Wert, wird durch das untere Bit der Summe von `summand1` und ersetzt `summand2` .</span><span class="sxs-lookup"><span data-stu-id="9263a-113">Second summand qubit, is replaced with the lower bit of the sum of `summand1` and `summand2`.</span></span>


### <a name="carryout--qubit"></a><span data-ttu-id="9263a-114">carryout: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="9263a-114">carryOut : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="9263a-115">"Qubit ausführen" ist ein XoReD mit dem höheren Bit der Summe.</span><span class="sxs-lookup"><span data-stu-id="9263a-115">Carry-out qubit, will be xored with the higher bit of the sum.</span></span>



## <a name="output--unit"></a><span data-ttu-id="9263a-116">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="9263a-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

