---
uid: Microsoft.Quantum.Arithmetic.ApplyInnerTTKAdderWithoutCarry
title: Applyinnerttkadderwithoutcarry-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyInnerTTKAdderWithoutCarry
qsharp.summary: Implements the inner addition function for the operation RippleCarryAdderNoCarryTTK. This is the inner operation that is conjugated with the outer operation to construct the full adder.
ms.openlocfilehash: 0c1626c788215181b5ed45dc98bed928b5e4848a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843811"
---
# <a name="applyinnerttkadderwithoutcarry-operation"></a><span data-ttu-id="e847f-102">Applyinnerttkadderwithoutcarry-Vorgang</span><span class="sxs-lookup"><span data-stu-id="e847f-102">ApplyInnerTTKAdderWithoutCarry operation</span></span>

<span data-ttu-id="e847f-103">Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="e847f-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="e847f-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="e847f-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="e847f-105">Implementiert die innere Additions Funktion für den Vorgang ripplecarryaddernocarryttk.</span><span class="sxs-lookup"><span data-stu-id="e847f-105">Implements the inner addition function for the operation RippleCarryAdderNoCarryTTK.</span></span> <span data-ttu-id="e847f-106">Dies ist der innere Vorgang, der mit dem äußeren Vorgang konjuregiert wird, um den vollständigen Adder zu konstruieren.</span><span class="sxs-lookup"><span data-stu-id="e847f-106">This is the inner operation that is conjugated with the outer operation to construct the full adder.</span></span>

```qsharp
operation ApplyInnerTTKAdderWithoutCarry (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="e847f-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e847f-107">Input</span></span>

### <a name="xs--littleendian"></a><span data-ttu-id="e847f-108">xs: [littleenddian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="e847f-108">xs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="e847f-109">"LittleEndian Qubit": Codierung der ersten ganzzahligen Summe und Eingabe in ripplecarryaddernocarryttk.</span><span class="sxs-lookup"><span data-stu-id="e847f-109">LittleEndian qubit register encoding the first integer summand input to RippleCarryAdderNoCarryTTK.</span></span>


### <a name="ys--littleendian"></a><span data-ttu-id="e847f-110">YS: [littleumdian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="e847f-110">ys : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="e847f-111">LittleEndian Qubit-Register Codierung der zweiten ganzzahligen Summe und Eingabe in ripplecarryaddernocarryttk.</span><span class="sxs-lookup"><span data-stu-id="e847f-111">LittleEndian qubit register encoding the second integer summand input to RippleCarryAdderNoCarryTTK.</span></span>



## <a name="output--unit"></a><span data-ttu-id="e847f-112">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="e847f-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="e847f-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e847f-113">Remarks</span></span>

<span data-ttu-id="e847f-114">Der angegebene kontrollierte Vorgang verwendet die Symmetrie und den gegenseitigen Abbruch von Vorgängen, um die Standard Implementierung zu verbessern, mit der jedem Vorgang ein Steuerelement hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="e847f-114">The specified controlled operation makes use of symmetry and mutual cancellation of operations to improve on the default implementation that adds a control to every operation.</span></span>

## <a name="references"></a><span data-ttu-id="e847f-115">References</span><span class="sxs-lookup"><span data-stu-id="e847f-115">References</span></span>

- <span data-ttu-id="e847f-116">Yasuhiro Takahashi, Seiichiro Tani, Noboru Kunihiro: "Quantum Additions-und ungebundene Fan-Out", Quantum-Informationen und-Berechnung, Vol. 10, 2010.</span><span class="sxs-lookup"><span data-stu-id="e847f-116">Yasuhiro Takahashi, Seiichiro Tani, Noboru Kunihiro: "Quantum Addition Circuits and Unbounded Fan-Out", Quantum Information and Computation, Vol. 10, 2010.</span></span>
  https://arxiv.org/abs/0910.2530