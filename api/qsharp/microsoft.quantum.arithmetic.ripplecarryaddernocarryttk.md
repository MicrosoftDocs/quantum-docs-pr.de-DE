---
uid: Microsoft.Quantum.Arithmetic.RippleCarryAdderNoCarryTTK
title: Ripplecarryaddernocarryttk-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: RippleCarryAdderNoCarryTTK
qsharp.summary: Reversible, in-place ripple-carry addition of two integers without carry out.
ms.openlocfilehash: 0e131204d3eaff7f99aa9ff7c3c1ae93a1bf611b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846347"
---
# <a name="ripplecarryaddernocarryttk-operation"></a><span data-ttu-id="b215a-102">Ripplecarryaddernocarryttk-Vorgang</span><span class="sxs-lookup"><span data-stu-id="b215a-102">RippleCarryAdderNoCarryTTK operation</span></span>

<span data-ttu-id="b215a-103">Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="b215a-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="b215a-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="b215a-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="b215a-105">Umkehrbar, direkte Ripple-Durchführung von zwei Ganzzahlen ohne Ausführung.</span><span class="sxs-lookup"><span data-stu-id="b215a-105">Reversible, in-place ripple-carry addition of two integers without carry out.</span></span>

```qsharp
operation RippleCarryAdderNoCarryTTK (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="b215a-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b215a-106">Description</span></span>

<span data-ttu-id="b215a-107">Bei zwei $n in den littleEndian-Registern und in den littleEndian-Registern codierten $-Bit-Ganzzahlen `xs` `ys` berechnet der Vorgang die Summe der beiden integger Modulo $2 ^ n $, wobei $n $ die bitgröße der Eingaben `xs` und ist `ys` .</span><span class="sxs-lookup"><span data-stu-id="b215a-107">Given two $n$-bit integers encoded in LittleEndian registers `xs` and `ys`, the operation computes the sum of the two integers modulo $2^n$, where $n$ is the bit size of the inputs `xs` and `ys`.</span></span> <span data-ttu-id="b215a-108">Das Bit wird nicht berechnet.</span><span class="sxs-lookup"><span data-stu-id="b215a-108">It does not compute the carry out bit.</span></span>

## <a name="input"></a><span data-ttu-id="b215a-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b215a-109">Input</span></span>

### <a name="xs--littleendian"></a><span data-ttu-id="b215a-110">xs: [littleenddian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="b215a-110">xs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="b215a-111">Der littleEndian-Qubit-Register Codierung der ersten ganzzahligen Summe.</span><span class="sxs-lookup"><span data-stu-id="b215a-111">LittleEndian qubit register encoding the first integer summand.</span></span>


### <a name="ys--littleendian"></a><span data-ttu-id="b215a-112">YS: [littleumdian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="b215a-112">ys : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="b215a-113">Der littleEndian-Qubit-Registrierungs Codierungs Wert für die zweite Ganzzahl sumund wird so geändert, dass die $n minimalen signifikanten Bits der Summe enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="b215a-113">LittleEndian qubit register encoding the second integer summand, is modified to hold the $n$ least significant bits of the sum.</span></span>



## <a name="output--unit"></a><span data-ttu-id="b215a-114">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="b215a-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="b215a-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b215a-115">Remarks</span></span>

<span data-ttu-id="b215a-116">Dieser Vorgang verfügt über die gleiche Funktionalität wie ripplecarryadderttk, gibt jedoch nicht das "Carry"-Bit zurück.</span><span class="sxs-lookup"><span data-stu-id="b215a-116">This operation has the same functionality as RippleCarryAdderTTK but does not return the carry bit.</span></span>

## <a name="references"></a><span data-ttu-id="b215a-117">References</span><span class="sxs-lookup"><span data-stu-id="b215a-117">References</span></span>

- <span data-ttu-id="b215a-118">Yasuhiro Takahashi, Seiichiro Tani, Noboru Kunihiro: "Quantum Additions-und ungebundene Fan-Out", Quantum-Informationen und-Berechnung, Vol. 10, 2010.</span><span class="sxs-lookup"><span data-stu-id="b215a-118">Yasuhiro Takahashi, Seiichiro Tani, Noboru Kunihiro: "Quantum Addition Circuits and Unbounded Fan-Out", Quantum Information and Computation, Vol. 10, 2010.</span></span>
  https://arxiv.org/abs/0910.2530