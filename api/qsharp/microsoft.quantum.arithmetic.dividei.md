---
uid: Microsoft.Quantum.Arithmetic.DivideI
title: Dividei-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: DivideI
qsharp.summary: Divides two quantum integers.
ms.openlocfilehash: 73c4e394ca38b8089b2990f8a8b6a3ee50f644d8
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846686"
---
# <a name="dividei-operation"></a><span data-ttu-id="86988-102">Dividei-Vorgang</span><span class="sxs-lookup"><span data-stu-id="86988-102">DivideI operation</span></span>

<span data-ttu-id="86988-103">Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="86988-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="86988-104">Paket: [Microsoft. Quantum. Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span><span class="sxs-lookup"><span data-stu-id="86988-104">Package: [Microsoft.Quantum.Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span></span>


<span data-ttu-id="86988-105">Dividiert zwei Quantum-Ganzzahlen.</span><span class="sxs-lookup"><span data-stu-id="86988-105">Divides two quantum integers.</span></span>

```qsharp
operation DivideI (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian, result : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="86988-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="86988-106">Description</span></span>

<span data-ttu-id="86988-107">`xs` hält den Rest `xs - floor(xs/ys) * ys` und `result` hält `floor(xs/ys)` .</span><span class="sxs-lookup"><span data-stu-id="86988-107">`xs` will hold the remainder `xs - floor(xs/ys) * ys` and `result` will hold `floor(xs/ys)`.</span></span>

## <a name="input"></a><span data-ttu-id="86988-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="86988-108">Input</span></span>

### <a name="xs--littleendian"></a><span data-ttu-id="86988-109">xs: [littleenddian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="86988-109">xs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="86988-110">$n $-Bit-Dividende wird durch den Rest ersetzt.</span><span class="sxs-lookup"><span data-stu-id="86988-110">$n$-bit dividend, will be replaced by the remainder.</span></span>


### <a name="ys--littleendian"></a><span data-ttu-id="86988-111">YS: [littleumdian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="86988-111">ys : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="86988-112">$n $-Bit-Divisor</span><span class="sxs-lookup"><span data-stu-id="86988-112">$n$-bit divisor</span></span>


### <a name="result--littleendian"></a><span data-ttu-id="86988-113">Ergebnis: [littleenddian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="86988-113">result : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="86988-114">$n $-Bit-Ergebnis muss zunächst den Status $ \ket {0} $ aufweisen und durch das Ergebnis der ganzzahligen Division ersetzt werden.</span><span class="sxs-lookup"><span data-stu-id="86988-114">$n$-bit result, must be in state $\ket{0}$ initially and will be replaced by the result of the integer division.</span></span>



## <a name="output--unit"></a><span data-ttu-id="86988-115">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="86988-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="86988-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="86988-116">Remarks</span></span>

<span data-ttu-id="86988-117">Verwendet einen standardmäßigen Shift-and-Subtract-Ansatz, um die Division zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="86988-117">Uses a standard shift-and-subtract approach to implement the division.</span></span>
<span data-ttu-id="86988-118">Die kontrollierte Version ist spezialisiert, sodass für die Subtraktion keine zusätzlichen Steuerelemente erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="86988-118">The controlled version is specialized such the subtraction does not require additional controls.</span></span>