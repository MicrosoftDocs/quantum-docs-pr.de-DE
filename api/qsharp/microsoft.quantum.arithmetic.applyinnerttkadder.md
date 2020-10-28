---
uid: Microsoft.Quantum.Arithmetic.ApplyInnerTTKAdder
title: Applyinnerttkadder-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyInnerTTKAdder
qsharp.summary: Implements the inner addition function for the operation RippleCarryAdderTTK. This is the inner operation that is conjugated with the outer operation to construct the full adder.
ms.openlocfilehash: 23c1f6dcdf3894cf1b416efd922c9eed01ac8f85
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707634"
---
# <a name="applyinnerttkadder-operation"></a><span data-ttu-id="f1735-102">Applyinnerttkadder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="f1735-102">ApplyInnerTTKAdder operation</span></span>

<span data-ttu-id="f1735-103">Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="f1735-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="f1735-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="f1735-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="f1735-105">Implementiert die innere Additions Funktion für den Vorgang ripplecarryadderttk.</span><span class="sxs-lookup"><span data-stu-id="f1735-105">Implements the inner addition function for the operation RippleCarryAdderTTK.</span></span> <span data-ttu-id="f1735-106">Dies ist der innere Vorgang, der mit dem äußeren Vorgang konjuregiert wird, um den vollständigen Adder zu konstruieren.</span><span class="sxs-lookup"><span data-stu-id="f1735-106">This is the inner operation that is conjugated with the outer operation to construct the full adder.</span></span>

```qsharp
operation ApplyInnerTTKAdder (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian, carry : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="f1735-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f1735-107">Input</span></span>

### <a name="xs--littleendian"></a><span data-ttu-id="f1735-108">xs: [littleenddian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="f1735-108">xs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="f1735-109">LittleEndian-Qubit-Registrierung Codieren der ersten ganzzahligen Summe und Eingabe in ripplecarryadderttk.</span><span class="sxs-lookup"><span data-stu-id="f1735-109">LittleEndian qubit register encoding the first integer summand input to RippleCarryAdderTTK.</span></span>


### <a name="ys--littleendian"></a><span data-ttu-id="f1735-110">YS: [littleumdian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="f1735-110">ys : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="f1735-111">LittleEndian Qubit-Register Codierung der zweiten ganzzahligen Summe und Eingabe in ripplecarryadderttk.</span><span class="sxs-lookup"><span data-stu-id="f1735-111">LittleEndian qubit register encoding the second integer summand input to RippleCarryAdderTTK.</span></span>


### <a name="carry--qubit"></a><span data-ttu-id="f1735-112">Carry: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="f1735-112">carry : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="f1735-113">Carry Qubit, ist XoReD mit dem signifikantesten Bit der Summe.</span><span class="sxs-lookup"><span data-stu-id="f1735-113">Carry qubit, is xored with the most significant bit of the sum.</span></span>



## <a name="output--unit"></a><span data-ttu-id="f1735-114">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="f1735-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="f1735-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f1735-115">Remarks</span></span>

<span data-ttu-id="f1735-116">Der angegebene kontrollierte Vorgang verwendet die Symmetrie und den gegenseitigen Abbruch von Vorgängen, um die Standard Implementierung zu verbessern, mit der jedem Vorgang ein Steuerelement hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="f1735-116">The specified controlled operation makes use of symmetry and mutual cancellation of operations to improve on the default implementation that adds a control to every operation.</span></span>

## <a name="references"></a><span data-ttu-id="f1735-117">Referenzen</span><span class="sxs-lookup"><span data-stu-id="f1735-117">References</span></span>

- <span data-ttu-id="f1735-118">Yasuhiro Takahashi, Seiichiro Tani, Noboru Kunihiro: "Quantum Additions-und ungebundene Fan-Out", Quantum-Informationen und-Berechnung, Vol. 10, 2010.</span><span class="sxs-lookup"><span data-stu-id="f1735-118">Yasuhiro Takahashi, Seiichiro Tani, Noboru Kunihiro: "Quantum Addition Circuits and Unbounded Fan-Out", Quantum Information and Computation, Vol. 10, 2010.</span></span>
  https://arxiv.org/abs/0910.2530