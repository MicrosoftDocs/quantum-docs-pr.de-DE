---
uid: Microsoft.Quantum.Arithmetic.SquareI
title: Squarei-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: SquareI
qsharp.summary: Computes the square of the integer `xs` into `result`, which must be zero initially.
ms.openlocfilehash: 6813c8144b0ac98bae404b5e9b97e08b06c6bb3a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846312"
---
# <a name="squarei-operation"></a><span data-ttu-id="5b822-102">Squarei-Vorgang</span><span class="sxs-lookup"><span data-stu-id="5b822-102">SquareI operation</span></span>

<span data-ttu-id="5b822-103">Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="5b822-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="5b822-104">Paket: [Microsoft. Quantum. Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span><span class="sxs-lookup"><span data-stu-id="5b822-104">Package: [Microsoft.Quantum.Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span></span>


<span data-ttu-id="5b822-105">Berechnet das Quadrat der Ganzzahl `xs` in `result` , das anfänglich NULL sein muss.</span><span class="sxs-lookup"><span data-stu-id="5b822-105">Computes the square of the integer `xs` into `result`, which must be zero initially.</span></span>

```qsharp
operation SquareI (xs : Microsoft.Quantum.Arithmetic.LittleEndian, result : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="5b822-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5b822-106">Input</span></span>

### <a name="xs--littleendian"></a><span data-ttu-id="5b822-107">xs: [littleenddian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="5b822-107">xs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="5b822-108">$n $-Bit-Nummer zum Quadrat (littleEndian)</span><span class="sxs-lookup"><span data-stu-id="5b822-108">$n$-bit number to square (LittleEndian)</span></span>


### <a name="result--littleendian"></a><span data-ttu-id="5b822-109">Ergebnis: [littleenddian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="5b822-109">result : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="5b822-110">$2N $-Bit-Ergebnis (littleEndian) muss zunächst den Status $ \ket {0} $ aufweisen.</span><span class="sxs-lookup"><span data-stu-id="5b822-110">$2n$-bit result (LittleEndian), must be in state $\ket{0}$ initially.</span></span>



## <a name="output--unit"></a><span data-ttu-id="5b822-111">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="5b822-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="5b822-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5b822-112">Remarks</span></span>

<span data-ttu-id="5b822-113">Verwendet einen standardmäßigen Shift-and-Add-Ansatz, um das Quadrat zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="5b822-113">Uses a standard shift-and-add approach to compute the square.</span></span> <span data-ttu-id="5b822-114">Speichert $n-$1-Qubits im Vergleich zur geradlinigen Projekt Mappe, die zuerst XS kopiert, bevor Sie einen regulären Multiplikator anwendet und dann den Kopiervorgang zurücknimmt.</span><span class="sxs-lookup"><span data-stu-id="5b822-114">Saves $n-1$ qubits compared to the straight-forward solution which first copies out xs before applying a regular multiplier and then undoing the copy operation.</span></span>