---
uid: Microsoft.Quantum.Arithmetic.RippleCarryAdderCDKM
title: Ripplecarryaddercdkm-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: RippleCarryAdderCDKM
qsharp.summary: Reversible, in-place ripple-carry addition of two integers.
ms.openlocfilehash: 6dcb5193c5d1d059682a79e63e6562aabff7539d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706271"
---
# <a name="ripplecarryaddercdkm-operation"></a><span data-ttu-id="d9fff-102">Ripplecarryaddercdkm-Vorgang</span><span class="sxs-lookup"><span data-stu-id="d9fff-102">RippleCarryAdderCDKM operation</span></span>

<span data-ttu-id="d9fff-103">Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="d9fff-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="d9fff-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="d9fff-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="d9fff-105">Umkehrbarer, direkter Ripple-Carry-Wert: Addition von zwei Ganzzahlen.</span><span class="sxs-lookup"><span data-stu-id="d9fff-105">Reversible, in-place ripple-carry addition of two integers.</span></span>

```qsharp
operation RippleCarryAdderCDKM (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian, carry : Qubit) : Unit
```


## <a name="description"></a><span data-ttu-id="d9fff-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d9fff-106">Description</span></span>

<span data-ttu-id="d9fff-107">Bei zwei $n ganzen Zahlen mit ganzen Zahlen, die in den littleEndian `xs` -Registern und `ys` , und einem Qubit-Wert codiert sind, berechnet der-Vorgang die Summe der beiden ganzen Zahlen, bei denen die $n $ geringsten signifikanten Bits des Ergebnisses in gespeichert sind `ys` und der Wert für das Ausführen von XoReD zum Qubit ist `carry` .</span><span class="sxs-lookup"><span data-stu-id="d9fff-107">Given two $n$-bit integers encoded in LittleEndian registers `xs` and `ys`, and a qubit carry, the operation computes the sum of the two integers where the $n$ least significant bits of the result are held in `ys` and the carry out bit is xored to the qubit `carry`.</span></span>

## <a name="input"></a><span data-ttu-id="d9fff-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d9fff-108">Input</span></span>

### <a name="xs--littleendian"></a><span data-ttu-id="d9fff-109">xs: [littleenddian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="d9fff-109">xs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="d9fff-110">Der littleEndian-Qubit-Register Codierung der ersten ganzzahligen Summe.</span><span class="sxs-lookup"><span data-stu-id="d9fff-110">LittleEndian qubit register encoding the first integer summand.</span></span>


### <a name="ys--littleendian"></a><span data-ttu-id="d9fff-111">YS: [littleumdian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="d9fff-111">ys : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="d9fff-112">Bei der littleEndian-Qubit-Codierung wird die zweite Ganzzahl summiert, und die n-Bit-Summe der Summe wird geändert.</span><span class="sxs-lookup"><span data-stu-id="d9fff-112">LittleEndian qubit register encoding the second integer summand, is modified to hold the n least significant bits of the sum.</span></span>


### <a name="carry--qubit"></a><span data-ttu-id="d9fff-113">Carry: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="d9fff-113">carry : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="d9fff-114">Carry Qubit, ist XoReD mit dem signifikantesten Bit der Summe.</span><span class="sxs-lookup"><span data-stu-id="d9fff-114">Carry qubit, is xored with the most significant bit of the sum.</span></span>



## <a name="output--unit"></a><span data-ttu-id="d9fff-115">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="d9fff-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="d9fff-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d9fff-116">Remarks</span></span>

<span data-ttu-id="d9fff-117">Dieser Vorgang verfügt über die gleiche Funktionalität wie ripplecarryadderd, verwendet jedoch nur ein zusätzliches Qubit anstelle von $n $.</span><span class="sxs-lookup"><span data-stu-id="d9fff-117">This operation has the same functionality as RippleCarryAdderD, but only uses one auxiliary qubit instead of $n$.</span></span>

## <a name="references"></a><span data-ttu-id="d9fff-118">Referenzen</span><span class="sxs-lookup"><span data-stu-id="d9fff-118">References</span></span>

- <span data-ttu-id="d9fff-119">Steven a. Cuccaro, Thomas G. Draper, Samuel A. KUTIN, David Petrie Moulton: "A New Quantum Ripple-Carry Additions Circuit", 2004.</span><span class="sxs-lookup"><span data-stu-id="d9fff-119">Steven A. Cuccaro, Thomas G. Draper, Samuel A. Kutin, David Petrie Moulton: "A new quantum ripple-carry addition circuit", 2004.</span></span>
  https://arxiv.org/abs/quant-ph/0410184v1