---
uid: Microsoft.Quantum.Arithmetic.Carry
title: Carry-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: Carry
qsharp.summary: Implements a reversible carry gate. Given a carry-in bit encoded in qubit `carryIn` and two summand bits encoded in `summand1` and `summand2`, computes the bitwise xor of `carryIn`, `summand1` and `summand2` in the qubit `summand2` and the carry-out is xored to the qubit `carryOut`.
ms.openlocfilehash: dfb08a9a9c805c0b611ab993c9b1eb949810a7da
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843350"
---
# <a name="carry-operation"></a><span data-ttu-id="dbad5-102">Carry-Vorgang</span><span class="sxs-lookup"><span data-stu-id="dbad5-102">Carry operation</span></span>

<span data-ttu-id="dbad5-103">Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="dbad5-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="dbad5-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="dbad5-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="dbad5-105">Implementiert ein umkehrbares durchführen.</span><span class="sxs-lookup"><span data-stu-id="dbad5-105">Implements a reversible carry gate.</span></span> <span data-ttu-id="dbad5-106">Wenn ein in Qubit codiertes `carryIn` und zwei Summen in und codiert `summand1` `summand2` sind, berechnet das bitweise XOR von `carryIn` `summand1` und `summand2` im Qubit, `summand2` und die Überführung wird im Qubit-Element als XoReD `carryOut` festgestellt.</span><span class="sxs-lookup"><span data-stu-id="dbad5-106">Given a carry-in bit encoded in qubit `carryIn` and two summand bits encoded in `summand1` and `summand2`, computes the bitwise xor of `carryIn`, `summand1` and `summand2` in the qubit `summand2` and the carry-out is xored to the qubit `carryOut`.</span></span>

```qsharp
operation Carry (carryIn : Qubit, summand1 : Qubit, summand2 : Qubit, carryOut : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="dbad5-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="dbad5-107">Input</span></span>

### <a name="carryin--qubit"></a><span data-ttu-id="dbad5-108">Carryin: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="dbad5-108">carryIn : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="dbad5-109">Ein-in-Qubit.</span><span class="sxs-lookup"><span data-stu-id="dbad5-109">Carry-in qubit.</span></span>


### <a name="summand1--qubit"></a><span data-ttu-id="dbad5-110">summand1: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="dbad5-110">summand1 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="dbad5-111">Erstes Summen-und Qubit-Wert.</span><span class="sxs-lookup"><span data-stu-id="dbad5-111">First summand qubit.</span></span>


### <a name="summand2--qubit"></a><span data-ttu-id="dbad5-112">summand2: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="dbad5-112">summand2 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="dbad5-113">Zweites Summen-und Qubit-Wert, wird durch das untere Bit der Summe von `summand1` und ersetzt `summand2` .</span><span class="sxs-lookup"><span data-stu-id="dbad5-113">Second summand qubit, is replaced with the lower bit of the sum of `summand1` and `summand2`.</span></span>


### <a name="carryout--qubit"></a><span data-ttu-id="dbad5-114">carryout: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="dbad5-114">carryOut : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="dbad5-115">"Qubit ausführen" ist ein XoReD mit dem höheren Bit der Summe.</span><span class="sxs-lookup"><span data-stu-id="dbad5-115">Carry-out qubit, will be xored with the higher bit of the sum.</span></span>



## <a name="output--unit"></a><span data-ttu-id="dbad5-116">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="dbad5-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

