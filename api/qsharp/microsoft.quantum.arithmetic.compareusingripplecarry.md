---
uid: Microsoft.Quantum.Arithmetic.CompareUsingRippleCarry
title: Compareusingripplecarry-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: CompareUsingRippleCarry
qsharp.summary: This operation tests if an integer represented by a register of qubits is greater than another integer, applying an XOR of the result onto an output qubit.
ms.openlocfilehash: 842e7ded1e38f4f6e01e79d2758e30afb85dd349
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707378"
---
# <a name="compareusingripplecarry-operation"></a><span data-ttu-id="66e01-102">Compareusingripplecarry-Vorgang</span><span class="sxs-lookup"><span data-stu-id="66e01-102">CompareUsingRippleCarry operation</span></span>

<span data-ttu-id="66e01-103">Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="66e01-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="66e01-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="66e01-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="66e01-105">Dieser Vorgang testet, ob eine ganze Zahl, die durch ein Register von Qubits dargestellt wird, größer als eine andere Ganzzahl ist, und wendet ein XOR des Ergebnisses auf ein Ausgabe-Qubit an.</span><span class="sxs-lookup"><span data-stu-id="66e01-105">This operation tests if an integer represented by a register of qubits is greater than another integer, applying an XOR of the result onto an output qubit.</span></span>

```qsharp
operation CompareUsingRippleCarry (x : Microsoft.Quantum.Arithmetic.LittleEndian, y : Microsoft.Quantum.Arithmetic.LittleEndian, output : Qubit) : Unit
```


## <a name="description"></a><span data-ttu-id="66e01-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="66e01-106">Description</span></span>

<span data-ttu-id="66e01-107">Bei zwei Ganzzahlen `x` `y` , die in gleich großen Qubit-Registern gespeichert sind, überprüft dieser Vorgang, ob Sie übereinstimmen `x > y` .</span><span class="sxs-lookup"><span data-stu-id="66e01-107">Given two integers `x` and `y` stored in equal-size qubit registers, this operation checks if they satisfy `x > y`.</span></span> <span data-ttu-id="66e01-108">True gibt an, dass 1 ein XoReD in ein Ausgabe-Qubit ist.</span><span class="sxs-lookup"><span data-stu-id="66e01-108">If true, 1 is XORed into an output qubit.</span></span> <span data-ttu-id="66e01-109">Andernfalls wird 0 in einem Ausgabe-Qubit als XoReD fest.</span><span class="sxs-lookup"><span data-stu-id="66e01-109">Otherwise, 0 is XORed into an output qubit.</span></span>
<span data-ttu-id="66e01-110">Mit anderen Worten: dieser Vorgang kann durch die einheitliche $ $ \begin{align} u\ket {x} \ Ket {y} \ Ket {z} = \ket{x}\ket{y}\ket{z\oplus (x>y)} dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="66e01-110">In other words, this operation can be represented by the unitary $$ \begin{align} U\ket{x}\ket{y}\ket{z} = \ket{x}\ket{y}\ket{z\oplus (x>y)}.</span></span>
<span data-ttu-id="66e01-111">\end{align} $ $</span><span class="sxs-lookup"><span data-stu-id="66e01-111">\end{align} $$</span></span>

## <a name="input"></a><span data-ttu-id="66e01-112">Eingabe</span><span class="sxs-lookup"><span data-stu-id="66e01-112">Input</span></span>

### <a name="x--littleendian"></a><span data-ttu-id="66e01-113">x: [littleandian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="66e01-113">x : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="66e01-114">Die erste zu vergleichende Zahl, die im `LittleEndian` Format in einem Qubit-Register gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="66e01-114">First number to be compared stored in `LittleEndian` format in a qubit register.</span></span>


### <a name="y--littleendian"></a><span data-ttu-id="66e01-115">y: [littleddian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="66e01-115">y : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="66e01-116">Die zweite zu vergleichende Zahl, die im `LittleEndian` Format in einem Qubit-Register gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="66e01-116">Second number to be compared stored in `LittleEndian` format in a qubit register.</span></span>


### <a name="output--qubit"></a><span data-ttu-id="66e01-117">Ausgabe: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="66e01-117">output : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="66e01-118">Ein Qubit, das das Ergebnis des Vergleichs $x>y $ speichert.</span><span class="sxs-lookup"><span data-stu-id="66e01-118">Qubit that stores the result of the comparison $x>y$.</span></span>



## <a name="output--unit"></a><span data-ttu-id="66e01-119">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="66e01-119">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="references"></a><span data-ttu-id="66e01-120">Referenzen</span><span class="sxs-lookup"><span data-stu-id="66e01-120">References</span></span>

- <span data-ttu-id="66e01-121">Eine neue Quantum Ripple-be Additions Verbindung Steven a. Cuccaro, Thomas G. Draper, Samuel A. KUTIN, David Petrie Moulton https://arxiv.org/abs/quant-ph/0410184</span><span class="sxs-lookup"><span data-stu-id="66e01-121">A new quantum ripple-carry addition circuit Steven A. Cuccaro, Thomas G. Draper, Samuel A. Kutin, David Petrie Moulton https://arxiv.org/abs/quant-ph/0410184</span></span>