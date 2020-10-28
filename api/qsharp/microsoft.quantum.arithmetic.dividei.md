---
uid: Microsoft.Quantum.Arithmetic.DivideI
title: Dividei-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: DivideI
qsharp.summary: Divides two quantum integers.
ms.openlocfilehash: 0cc16dddc27a000dbc30de6ae27976a01fd9f4ed
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707343"
---
# <a name="dividei-operation"></a><span data-ttu-id="aa1be-102">Dividei-Vorgang</span><span class="sxs-lookup"><span data-stu-id="aa1be-102">DivideI operation</span></span>

<span data-ttu-id="aa1be-103">Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="aa1be-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="aa1be-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="aa1be-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="aa1be-105">Dividiert zwei Quantum-Ganzzahlen.</span><span class="sxs-lookup"><span data-stu-id="aa1be-105">Divides two quantum integers.</span></span>

```qsharp
operation DivideI (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian, result : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="description"></a><span data-ttu-id="aa1be-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="aa1be-106">Description</span></span>

<span data-ttu-id="aa1be-107">`xs` hält den Rest `xs - floor(xs/ys) * ys` und `result` hält `floor(xs/ys)` .</span><span class="sxs-lookup"><span data-stu-id="aa1be-107">`xs` will hold the remainder `xs - floor(xs/ys) * ys` and `result` will hold `floor(xs/ys)`.</span></span>

## <a name="input"></a><span data-ttu-id="aa1be-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="aa1be-108">Input</span></span>

### <a name="xs--littleendian"></a><span data-ttu-id="aa1be-109">xs: [littleenddian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="aa1be-109">xs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="aa1be-110">$n $-Bit-Dividende wird durch den Rest ersetzt.</span><span class="sxs-lookup"><span data-stu-id="aa1be-110">$n$-bit dividend, will be replaced by the remainder.</span></span>


### <a name="ys--littleendian"></a><span data-ttu-id="aa1be-111">YS: [littleumdian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="aa1be-111">ys : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="aa1be-112">$n $-Bit-Divisor</span><span class="sxs-lookup"><span data-stu-id="aa1be-112">$n$-bit divisor</span></span>


### <a name="result--littleendian"></a><span data-ttu-id="aa1be-113">Ergebnis: [littleenddian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="aa1be-113">result : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="aa1be-114">$n $-Bit-Ergebnis muss zunächst den Status $ \ket {0} $ aufweisen und durch das Ergebnis der ganzzahligen Division ersetzt werden.</span><span class="sxs-lookup"><span data-stu-id="aa1be-114">$n$-bit result, must be in state $\ket{0}$ initially and will be replaced by the result of the integer division.</span></span>



## <a name="output--unit"></a><span data-ttu-id="aa1be-115">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="aa1be-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="aa1be-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="aa1be-116">Remarks</span></span>

<span data-ttu-id="aa1be-117">Verwendet einen standardmäßigen Shift-and-Subtract-Ansatz, um die Division zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="aa1be-117">Uses a standard shift-and-subtract approach to implement the division.</span></span>
<span data-ttu-id="aa1be-118">Die kontrollierte Version ist spezialisiert, sodass für die Subtraktion keine zusätzlichen Steuerelemente erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="aa1be-118">The controlled version is specialized such the subtraction does not require additional controls.</span></span>