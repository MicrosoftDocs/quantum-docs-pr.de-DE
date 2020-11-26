---
uid: Microsoft.Quantum.Arithmetic.RippleCarryAdderCDKM
title: Ripplecarryaddercdkm-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: RippleCarryAdderCDKM
qsharp.summary: Reversible, in-place ripple-carry addition of two integers.
ms.openlocfilehash: b08d8823fd539263205aca1ee15ee69adcb163b7
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96222098"
---
# <a name="ripplecarryaddercdkm-operation"></a><span data-ttu-id="90528-102">Ripplecarryaddercdkm-Vorgang</span><span class="sxs-lookup"><span data-stu-id="90528-102">RippleCarryAdderCDKM operation</span></span>

<span data-ttu-id="90528-103">Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="90528-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="90528-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="90528-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="90528-105">Umkehrbarer, direkter Ripple-Carry-Wert: Addition von zwei Ganzzahlen.</span><span class="sxs-lookup"><span data-stu-id="90528-105">Reversible, in-place ripple-carry addition of two integers.</span></span>

```qsharp
operation RippleCarryAdderCDKM (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian, carry : Qubit) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="90528-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="90528-106">Description</span></span>

<span data-ttu-id="90528-107">Bei zwei $n ganzen Zahlen mit ganzen Zahlen, die in den littleEndian `xs` -Registern und `ys` , und einem Qubit-Wert codiert sind, berechnet der-Vorgang die Summe der beiden ganzen Zahlen, bei denen die $n $ geringsten signifikanten Bits des Ergebnisses in gespeichert sind `ys` und der Wert für das Ausführen von XoReD zum Qubit ist `carry` .</span><span class="sxs-lookup"><span data-stu-id="90528-107">Given two $n$-bit integers encoded in LittleEndian registers `xs` and `ys`, and a qubit carry, the operation computes the sum of the two integers where the $n$ least significant bits of the result are held in `ys` and the carry out bit is xored to the qubit `carry`.</span></span>

## <a name="input"></a><span data-ttu-id="90528-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="90528-108">Input</span></span>

### <a name="xs--littleendian"></a><span data-ttu-id="90528-109">xs: [littleenddian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="90528-109">xs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="90528-110">Der littleEndian-Qubit-Register Codierung der ersten ganzzahligen Summe.</span><span class="sxs-lookup"><span data-stu-id="90528-110">LittleEndian qubit register encoding the first integer summand.</span></span>


### <a name="ys--littleendian"></a><span data-ttu-id="90528-111">YS: [littleumdian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="90528-111">ys : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="90528-112">Bei der littleEndian-Qubit-Codierung wird die zweite Ganzzahl summiert, und die n-Bit-Summe der Summe wird geändert.</span><span class="sxs-lookup"><span data-stu-id="90528-112">LittleEndian qubit register encoding the second integer summand, is modified to hold the n least significant bits of the sum.</span></span>


### <a name="carry--qubit"></a><span data-ttu-id="90528-113">Carry: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="90528-113">carry : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="90528-114">Carry Qubit, ist XoReD mit dem signifikantesten Bit der Summe.</span><span class="sxs-lookup"><span data-stu-id="90528-114">Carry qubit, is xored with the most significant bit of the sum.</span></span>



## <a name="output--unit"></a><span data-ttu-id="90528-115">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="90528-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="90528-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="90528-116">Remarks</span></span>

<span data-ttu-id="90528-117">Dieser Vorgang verfügt über die gleiche Funktionalität wie ripplecarryadderd, verwendet jedoch nur ein zusätzliches Qubit anstelle von $n $.</span><span class="sxs-lookup"><span data-stu-id="90528-117">This operation has the same functionality as RippleCarryAdderD, but only uses one auxiliary qubit instead of $n$.</span></span>

## <a name="references"></a><span data-ttu-id="90528-118">Referenzen</span><span class="sxs-lookup"><span data-stu-id="90528-118">References</span></span>

- <span data-ttu-id="90528-119">Steven a. Cuccaro, Thomas G. Draper, Samuel A. KUTIN, David Petrie Moulton: "A New Quantum Ripple-Carry Additions Circuit", 2004.</span><span class="sxs-lookup"><span data-stu-id="90528-119">Steven A. Cuccaro, Thomas G. Draper, Samuel A. Kutin, David Petrie Moulton: "A new quantum ripple-carry addition circuit", 2004.</span></span>
  https://arxiv.org/abs/quant-ph/0410184v1