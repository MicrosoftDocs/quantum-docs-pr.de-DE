---
uid: Microsoft.Quantum.Arithmetic.RippleCarryAdderD
title: Ripplecarryadderd-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: RippleCarryAdderD
qsharp.summary: Reversible, in-place ripple-carry addition of two integers. Given two $n$-bit integers encoded in LittleEndian registers `xs` and `ys`, and a qubit carry, the operation computes the sum of the two integers where the $n$ least significant bits of the result are held in `ys` and the carry out bit is xored to the qubit `carry`.
ms.openlocfilehash: b87c8f25acc8854d5e8d28f58cfc99dffb92a973
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96222115"
---
# <a name="ripplecarryadderd-operation"></a><span data-ttu-id="7efff-102">Ripplecarryadderd-Vorgang</span><span class="sxs-lookup"><span data-stu-id="7efff-102">RippleCarryAdderD operation</span></span>

<span data-ttu-id="7efff-103">Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="7efff-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="7efff-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="7efff-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="7efff-105">Umkehrbarer, direkter Ripple-Carry-Wert: Addition von zwei Ganzzahlen.</span><span class="sxs-lookup"><span data-stu-id="7efff-105">Reversible, in-place ripple-carry addition of two integers.</span></span>
<span data-ttu-id="7efff-106">Bei zwei $n ganzen Zahlen mit ganzen Zahlen, die in den littleEndian `xs` -Registern und `ys` , und einem Qubit-Wert codiert sind, berechnet der-Vorgang die Summe der beiden ganzen Zahlen, bei denen die $n $ geringsten signifikanten Bits des Ergebnisses in gespeichert sind `ys` und der Wert für das Ausführen von XoReD zum Qubit ist `carry` .</span><span class="sxs-lookup"><span data-stu-id="7efff-106">Given two $n$-bit integers encoded in LittleEndian registers `xs` and `ys`, and a qubit carry, the operation computes the sum of the two integers where the $n$ least significant bits of the result are held in `ys` and the carry out bit is xored to the qubit `carry`.</span></span>

```qsharp
operation RippleCarryAdderD (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian, carry : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="7efff-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="7efff-107">Input</span></span>

### <a name="xs--littleendian"></a><span data-ttu-id="7efff-108">xs: [littleenddian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="7efff-108">xs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="7efff-109">Der littleEndian-Qubit-Register Codierung der ersten ganzzahligen Summe.</span><span class="sxs-lookup"><span data-stu-id="7efff-109">LittleEndian qubit register encoding the first integer summand.</span></span>


### <a name="ys--littleendian"></a><span data-ttu-id="7efff-110">YS: [littleumdian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="7efff-110">ys : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="7efff-111">Der littleEndian-Qubit-Registrierungs Codierungs Wert für die zweite Ganzzahl sumund wird so geändert, dass die $n minimalen signifikanten Bits der Summe enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="7efff-111">LittleEndian qubit register encoding the second integer summand, is modified to hold the $n$ least significant bits of the sum.</span></span>


### <a name="carry--qubit"></a><span data-ttu-id="7efff-112">Carry: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="7efff-112">carry : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="7efff-113">Carry Qubit, ist XoReD mit dem signifikantesten Bit der Summe.</span><span class="sxs-lookup"><span data-stu-id="7efff-113">Carry qubit, is xored with the most significant bit of the sum.</span></span>



## <a name="output--unit"></a><span data-ttu-id="7efff-114">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="7efff-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="7efff-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7efff-115">Remarks</span></span>

<span data-ttu-id="7efff-116">Der angegebene kontrollierte Vorgang verwendet die Symmetrie und den gegenseitigen Abbruch von Vorgängen, um die Standard Implementierung zu verbessern, mit der jedem Vorgang ein Steuerelement hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="7efff-116">The specified controlled operation makes use of symmetry and mutual cancellation of operations to improve on the default implementation that adds a control to every operation.</span></span>

## <a name="references"></a><span data-ttu-id="7efff-117">Referenzen</span><span class="sxs-lookup"><span data-stu-id="7efff-117">References</span></span>

- <span data-ttu-id="7efff-118">Thomas G. Draper: "Addition auf einem Quantum-Computer", 2000.</span><span class="sxs-lookup"><span data-stu-id="7efff-118">Thomas G. Draper: "Addition on a Quantum Computer", 2000.</span></span>
  https://arxiv.org/abs/quant-ph/0008033