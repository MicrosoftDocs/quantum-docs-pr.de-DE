---
uid: Microsoft.Quantum.Arithmetic.ApplyOuterCDKMAdder
title: Applyoutercdkmadder-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyOuterCDKMAdder
qsharp.summary: Reversible, in-place ripple-carry operation that is used in the integer addition operation RippleCarryAdderCDKM below. Given two qubit registers `xs` and `ys` of the same length, the operation applies a ripple carry sequence of CNOT and CCNOT gates with qubits in `xs` and `ys` as the controls and qubits in `xs` as the targets.
ms.openlocfilehash: acaa563245bb7c701316d2dfd35b5be03d8e024d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843708"
---
# <a name="applyoutercdkmadder-operation"></a><span data-ttu-id="0e308-102">Applyoutercdkmadder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="0e308-102">ApplyOuterCDKMAdder operation</span></span>

<span data-ttu-id="0e308-103">Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="0e308-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="0e308-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="0e308-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="0e308-105">Umkehrbarer, direkter Ripple-Operation-Vorgang, der in der ganzzahligen Additions Operation ripplecarryaddercdkm weiter unten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0e308-105">Reversible, in-place ripple-carry operation that is used in the integer addition operation RippleCarryAdderCDKM below.</span></span>
<span data-ttu-id="0e308-106">Bei zwei Qubit `xs` -Registern und `ys` derselben Länge wendet der-Vorgang eine Ripple-Sequenz Sequenz von "CNOT" und "ccnot Gates" mit Qubits in `xs` und als die Ziele an `ys` `xs` .</span><span class="sxs-lookup"><span data-stu-id="0e308-106">Given two qubit registers `xs` and `ys` of the same length, the operation applies a ripple carry sequence of CNOT and CCNOT gates with qubits in `xs` and `ys` as the controls and qubits in `xs` as the targets.</span></span>

```qsharp
operation ApplyOuterCDKMAdder (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian, ancilla : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="0e308-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0e308-107">Input</span></span>

### <a name="xs--littleendian"></a><span data-ttu-id="0e308-108">xs: [littleenddian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="0e308-108">xs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="0e308-109">Erstes Qubit-Register, das Steuerelemente und Ziele enthält.</span><span class="sxs-lookup"><span data-stu-id="0e308-109">First qubit register, containing controls and targets.</span></span>


### <a name="ys--littleendian"></a><span data-ttu-id="0e308-110">YS: [littleumdian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="0e308-110">ys : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="0e308-111">Zweites Qubit-Register, das zu den Steuerelementen beiträgt.</span><span class="sxs-lookup"><span data-stu-id="0e308-111">Second qubit register, contributing to the controls.</span></span>


### <a name="ancilla--qubit"></a><span data-ttu-id="0e308-112">Ancilla: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="0e308-112">ancilla : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="0e308-113">Das in ripplecarryaddercdkm verwendete Ancilla-Qubit, das an diesen Vorgang übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="0e308-113">The ancilla qubit used in RippleCarryAdderCDKM passed to this operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="0e308-114">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="0e308-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="references"></a><span data-ttu-id="0e308-115">References</span><span class="sxs-lookup"><span data-stu-id="0e308-115">References</span></span>

- <span data-ttu-id="0e308-116">Steven a. Cuccaro, Thomas G. Draper, Samuel A. KUTIN, David Petrie Moulton: "A New Quantum Ripple-Carry Additions Circuit", 2004.</span><span class="sxs-lookup"><span data-stu-id="0e308-116">Steven A. Cuccaro, Thomas G. Draper, Samuel A. Kutin, David Petrie Moulton: "A new quantum ripple-carry addition circuit", 2004.</span></span>
  https://arxiv.org/abs/quant-ph/0410184v1