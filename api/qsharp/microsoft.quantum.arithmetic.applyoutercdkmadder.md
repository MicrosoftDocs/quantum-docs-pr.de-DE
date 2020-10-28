---
uid: Microsoft.Quantum.Arithmetic.ApplyOuterCDKMAdder
title: Applyoutercdkmadder-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyOuterCDKMAdder
qsharp.summary: Reversible, in-place ripple-carry operation that is used in the integer addition operation RippleCarryAdderCDKM below. Given two qubit registers `xs` and `ys` of the same length, the operation applies a ripple carry sequence of CNOT and CCNOT gates with qubits in `xs` and `ys` as the controls and qubits in `xs` as the targets.
ms.openlocfilehash: 5ec9d31252254e40efb22e06656294325b4cffcd
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707575"
---
# <a name="applyoutercdkmadder-operation"></a><span data-ttu-id="29281-102">Applyoutercdkmadder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="29281-102">ApplyOuterCDKMAdder operation</span></span>

<span data-ttu-id="29281-103">Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="29281-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="29281-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="29281-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="29281-105">Umkehrbarer, direkter Ripple-Operation-Vorgang, der in der ganzzahligen Additions Operation ripplecarryaddercdkm weiter unten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="29281-105">Reversible, in-place ripple-carry operation that is used in the integer addition operation RippleCarryAdderCDKM below.</span></span>
<span data-ttu-id="29281-106">Bei zwei Qubit `xs` -Registern und `ys` derselben Länge wendet der-Vorgang eine Ripple-Sequenz Sequenz von "CNOT" und "ccnot Gates" mit Qubits in `xs` und als die Ziele an `ys` `xs` .</span><span class="sxs-lookup"><span data-stu-id="29281-106">Given two qubit registers `xs` and `ys` of the same length, the operation applies a ripple carry sequence of CNOT and CCNOT gates with qubits in `xs` and `ys` as the controls and qubits in `xs` as the targets.</span></span>

```qsharp
operation ApplyOuterCDKMAdder (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian, ancilla : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="29281-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="29281-107">Input</span></span>

### <a name="xs--littleendian"></a><span data-ttu-id="29281-108">xs: [littleenddian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="29281-108">xs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="29281-109">Erstes Qubit-Register, das Steuerelemente und Ziele enthält.</span><span class="sxs-lookup"><span data-stu-id="29281-109">First qubit register, containing controls and targets.</span></span>


### <a name="ys--littleendian"></a><span data-ttu-id="29281-110">YS: [littleumdian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="29281-110">ys : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="29281-111">Zweites Qubit-Register, das zu den Steuerelementen beiträgt.</span><span class="sxs-lookup"><span data-stu-id="29281-111">Second qubit register, contributing to the controls.</span></span>


### <a name="ancilla--qubit"></a><span data-ttu-id="29281-112">Ancilla: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="29281-112">ancilla : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="29281-113">Das in ripplecarryaddercdkm verwendete Ancilla-Qubit, das an diesen Vorgang übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="29281-113">The ancilla qubit used in RippleCarryAdderCDKM passed to this operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="29281-114">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="29281-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="references"></a><span data-ttu-id="29281-115">Referenzen</span><span class="sxs-lookup"><span data-stu-id="29281-115">References</span></span>

- <span data-ttu-id="29281-116">Steven a. Cuccaro, Thomas G. Draper, Samuel A. KUTIN, David Petrie Moulton: "A New Quantum Ripple-Carry Additions Circuit", 2004.</span><span class="sxs-lookup"><span data-stu-id="29281-116">Steven A. Cuccaro, Thomas G. Draper, Samuel A. Kutin, David Petrie Moulton: "A new quantum ripple-carry addition circuit", 2004.</span></span>
  https://arxiv.org/abs/quant-ph/0410184v1