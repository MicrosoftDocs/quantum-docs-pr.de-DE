---
uid: Microsoft.Quantum.Arithmetic.ApplyOuterTTKAdder
title: Applyouterttkadder-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyOuterTTKAdder
qsharp.summary: Implements the outer operation for RippleCarryAdderTTK to conjugate the inner operation to construct the full adder.
ms.openlocfilehash: 3d6d7c3446075130e5a8ee93abbd27e617d50b3b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707570"
---
# <a name="applyouterttkadder-operation"></a><span data-ttu-id="76369-102">Applyouterttkadder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="76369-102">ApplyOuterTTKAdder operation</span></span>

<span data-ttu-id="76369-103">Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="76369-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="76369-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="76369-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="76369-105">Implementiert den äußeren Vorgang für ripplecarryadderttk, um den inneren Vorgang zum Erstellen des vollständigen Adder konjugieren.</span><span class="sxs-lookup"><span data-stu-id="76369-105">Implements the outer operation for RippleCarryAdderTTK to conjugate the inner operation to construct the full adder.</span></span>

```qsharp
operation ApplyOuterTTKAdder (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="input"></a><span data-ttu-id="76369-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="76369-106">Input</span></span>

### <a name="xs--littleendian"></a><span data-ttu-id="76369-107">xs: [littleenddian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="76369-107">xs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="76369-108">LittleEndian-Qubit-Registrierung Codieren der ersten ganzzahligen Summe und Eingabe in ripplecarryadderttk.</span><span class="sxs-lookup"><span data-stu-id="76369-108">LittleEndian qubit register encoding the first integer summand input to RippleCarryAdderTTK.</span></span>


### <a name="ys--littleendian"></a><span data-ttu-id="76369-109">YS: [littleumdian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="76369-109">ys : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="76369-110">LittleEndian Qubit-Register Codierung der zweiten ganzzahligen Summe und Eingabe in ripplecarryadderttk.</span><span class="sxs-lookup"><span data-stu-id="76369-110">LittleEndian qubit register encoding the second integer summand input to RippleCarryAdderTTK.</span></span>



## <a name="output--unit"></a><span data-ttu-id="76369-111">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="76369-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="references"></a><span data-ttu-id="76369-112">Referenzen</span><span class="sxs-lookup"><span data-stu-id="76369-112">References</span></span>

- <span data-ttu-id="76369-113">Yasuhiro Takahashi, Seiichiro Tani, Noboru Kunihiro: "Quantum Additions-und ungebundene Fan-Out", Quantum-Informationen und-Berechnung, Vol. 10, 2010.</span><span class="sxs-lookup"><span data-stu-id="76369-113">Yasuhiro Takahashi, Seiichiro Tani, Noboru Kunihiro: "Quantum Addition Circuits and Unbounded Fan-Out", Quantum Information and Computation, Vol. 10, 2010.</span></span>
  https://arxiv.org/abs/0910.2530