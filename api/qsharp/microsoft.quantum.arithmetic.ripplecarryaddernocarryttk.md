---
uid: Microsoft.Quantum.Arithmetic.RippleCarryAdderNoCarryTTK
title: Ripplecarryaddernocarryttk-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: RippleCarryAdderNoCarryTTK
qsharp.summary: Reversible, in-place ripple-carry addition of two integers without carry out.
ms.openlocfilehash: 59451b4f5c992f900a27139332059af7427b9b93
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706250"
---
# <a name="ripplecarryaddernocarryttk-operation"></a><span data-ttu-id="cd7ec-102">Ripplecarryaddernocarryttk-Vorgang</span><span class="sxs-lookup"><span data-stu-id="cd7ec-102">RippleCarryAdderNoCarryTTK operation</span></span>

<span data-ttu-id="cd7ec-103">Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="cd7ec-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="cd7ec-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="cd7ec-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="cd7ec-105">Umkehrbar, direkte Ripple-Durchführung von zwei Ganzzahlen ohne Ausführung.</span><span class="sxs-lookup"><span data-stu-id="cd7ec-105">Reversible, in-place ripple-carry addition of two integers without carry out.</span></span>

```qsharp
operation RippleCarryAdderNoCarryTTK (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="description"></a><span data-ttu-id="cd7ec-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cd7ec-106">Description</span></span>

<span data-ttu-id="cd7ec-107">Bei zwei $n in den littleEndian-Registern und in den littleEndian-Registern codierten $-Bit-Ganzzahlen `xs` `ys` berechnet der Vorgang die Summe der beiden integger Modulo $2 ^ n $, wobei $n $ die bitgröße der Eingaben `xs` und ist `ys` .</span><span class="sxs-lookup"><span data-stu-id="cd7ec-107">Given two $n$-bit integers encoded in LittleEndian registers `xs` and `ys`, the operation computes the sum of the two integers modulo $2^n$, where $n$ is the bit size of the inputs `xs` and `ys`.</span></span> <span data-ttu-id="cd7ec-108">Das Bit wird nicht berechnet.</span><span class="sxs-lookup"><span data-stu-id="cd7ec-108">It does not compute the carry out bit.</span></span>

## <a name="input"></a><span data-ttu-id="cd7ec-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="cd7ec-109">Input</span></span>

### <a name="xs--littleendian"></a><span data-ttu-id="cd7ec-110">xs: [littleenddian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="cd7ec-110">xs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="cd7ec-111">Der littleEndian-Qubit-Register Codierung der ersten ganzzahligen Summe.</span><span class="sxs-lookup"><span data-stu-id="cd7ec-111">LittleEndian qubit register encoding the first integer summand.</span></span>


### <a name="ys--littleendian"></a><span data-ttu-id="cd7ec-112">YS: [littleumdian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="cd7ec-112">ys : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="cd7ec-113">Der littleEndian-Qubit-Registrierungs Codierungs Wert für die zweite Ganzzahl sumund wird so geändert, dass die $n minimalen signifikanten Bits der Summe enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="cd7ec-113">LittleEndian qubit register encoding the second integer summand, is modified to hold the $n$ least significant bits of the sum.</span></span>



## <a name="output--unit"></a><span data-ttu-id="cd7ec-114">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="cd7ec-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="cd7ec-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="cd7ec-115">Remarks</span></span>

<span data-ttu-id="cd7ec-116">Dieser Vorgang verfügt über die gleiche Funktionalität wie ripplecarryadderttk, gibt jedoch nicht das "Carry"-Bit zurück.</span><span class="sxs-lookup"><span data-stu-id="cd7ec-116">This operation has the same functionality as RippleCarryAdderTTK but does not return the carry bit.</span></span>

## <a name="references"></a><span data-ttu-id="cd7ec-117">Referenzen</span><span class="sxs-lookup"><span data-stu-id="cd7ec-117">References</span></span>

- <span data-ttu-id="cd7ec-118">Yasuhiro Takahashi, Seiichiro Tani, Noboru Kunihiro: "Quantum Additions-und ungebundene Fan-Out", Quantum-Informationen und-Berechnung, Vol. 10, 2010.</span><span class="sxs-lookup"><span data-stu-id="cd7ec-118">Yasuhiro Takahashi, Seiichiro Tani, Noboru Kunihiro: "Quantum Addition Circuits and Unbounded Fan-Out", Quantum Information and Computation, Vol. 10, 2010.</span></span>
  https://arxiv.org/abs/0910.2530