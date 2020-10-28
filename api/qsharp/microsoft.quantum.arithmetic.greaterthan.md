---
uid: Microsoft.Quantum.Arithmetic.GreaterThan
title: GreaterThan-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: GreaterThan
qsharp.summary: Applies a greater-than comparison between two integers encoded into qubit registers, flipping a target qubit based on the result of the comparison.
ms.openlocfilehash: b7214b43dacd07b4750be4b681f30937185ac953
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707287"
---
# <a name="greaterthan-operation"></a><span data-ttu-id="13b5a-102">GreaterThan-Vorgang</span><span class="sxs-lookup"><span data-stu-id="13b5a-102">GreaterThan operation</span></span>

<span data-ttu-id="13b5a-103">Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="13b5a-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="13b5a-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="13b5a-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="13b5a-105">Wendet einen größer-als-Vergleich zwischen zwei ganzen Zahlen an, die in Qubit-Registern codiert sind, wobei ein Ziel-Qubit basierend auf dem Ergebnis des Vergleichs geflippt wird.</span><span class="sxs-lookup"><span data-stu-id="13b5a-105">Applies a greater-than comparison between two integers encoded into qubit registers, flipping a target qubit based on the result of the comparison.</span></span>

```qsharp
operation GreaterThan (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian, result : Qubit) : Unit
```


## <a name="description"></a><span data-ttu-id="13b5a-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="13b5a-106">Description</span></span>

<span data-ttu-id="13b5a-107">Führt einen streng größeren Vergleich von zwei Ganzzahlen $x $ und $y $ aus, codiert in Qubit-Register XS und YS.</span><span class="sxs-lookup"><span data-stu-id="13b5a-107">Carries out a strictly greater than comparison of two integers $x$ and $y$, encoded in qubit registers xs and ys.</span></span> <span data-ttu-id="13b5a-108">Wenn $x > y $, wird das Ergebnis-Qubit gekippt, andernfalls behält das Qubit-Ergebnis den Zustand bei.</span><span class="sxs-lookup"><span data-stu-id="13b5a-108">If $x > y$, then the result qubit will be flipped, otherwise the result qubit will retain its state.</span></span>

## <a name="input"></a><span data-ttu-id="13b5a-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="13b5a-109">Input</span></span>

### <a name="xs--littleendian"></a><span data-ttu-id="13b5a-110">xs: [littleenddian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="13b5a-110">xs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="13b5a-111">LittleEndian-Qubit-Register Codierung der ersten Ganzzahl $x $.</span><span class="sxs-lookup"><span data-stu-id="13b5a-111">LittleEndian qubit register encoding the first integer $x$.</span></span>


### <a name="ys--littleendian"></a><span data-ttu-id="13b5a-112">YS: [littleumdian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="13b5a-112">ys : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="13b5a-113">LittleEndian Qubit-Register Codierung der zweiten Ganzzahl $y $.</span><span class="sxs-lookup"><span data-stu-id="13b5a-113">LittleEndian qubit register encoding the second integer $y$.</span></span>


### <a name="result--qubit"></a><span data-ttu-id="13b5a-114">Ergebnis: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="13b5a-114">result : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="13b5a-115">Einzelnes Qubit, das beim $x > y $ gekippt wird.</span><span class="sxs-lookup"><span data-stu-id="13b5a-115">Single qubit that will be flipped if $x > y$.</span></span>



## <a name="output--unit"></a><span data-ttu-id="13b5a-116">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="13b5a-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="13b5a-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="13b5a-117">Remarks</span></span>

<span data-ttu-id="13b5a-118">Verwendet den Trick, bei dem $x-y = (x ' + y) ' $, WHERE ' das Einerkomplement bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="13b5a-118">Uses the trick that $x - y = (x'+y)'$, where ' denotes the one's complement.</span></span>

## <a name="references"></a><span data-ttu-id="13b5a-119">Referenzen</span><span class="sxs-lookup"><span data-stu-id="13b5a-119">References</span></span>

- <span data-ttu-id="13b5a-120">Steven a. Cuccaro, Thomas G. Draper, Samuel A. KUTIN, David Petrie Moulton: "A New Quantum Ripple-Carry Additions Circuit", 2004.</span><span class="sxs-lookup"><span data-stu-id="13b5a-120">Steven A. Cuccaro, Thomas G. Draper, Samuel A. Kutin, David Petrie Moulton: "A new quantum ripple-carry addition circuit", 2004.</span></span>
  https://arxiv.org/abs/quant-ph/0410184v1

- <span data-ttu-id="13b5a-121">Thomas Haener, Martin roetteler, Krysta M. svore: "Factoring using 2N + 2 Qubits with Toffoli based modulare Multiplikation", 2016 https://arxiv.org/abs/1611.07995</span><span class="sxs-lookup"><span data-stu-id="13b5a-121">Thomas Haener, Martin Roetteler, Krysta M. Svore: "Factoring using 2n+2 qubits with Toffoli based modular multiplication", 2016 https://arxiv.org/abs/1611.07995</span></span>