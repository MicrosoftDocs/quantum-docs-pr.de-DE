---
uid: Microsoft.Quantum.Arithmetic.CompareGTI
title: Comparegti-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: CompareGTI
qsharp.summary: 'Wrapper for integer comparison: `result = x > y`.'
ms.openlocfilehash: e9c245fb7c0cf3a6b1b98eb01cd582c325917602
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843297"
---
# <a name="comparegti-operation"></a><span data-ttu-id="049af-102">Comparegti-Vorgang</span><span class="sxs-lookup"><span data-stu-id="049af-102">CompareGTI operation</span></span>

<span data-ttu-id="049af-103">Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="049af-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="049af-104">Paket: [Microsoft. Quantum. Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span><span class="sxs-lookup"><span data-stu-id="049af-104">Package: [Microsoft.Quantum.Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span></span>


<span data-ttu-id="049af-105">Wrapper für ganzzahligen Vergleich: `result = x > y` .</span><span class="sxs-lookup"><span data-stu-id="049af-105">Wrapper for integer comparison: `result = x > y`.</span></span>

```qsharp
operation CompareGTI (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian, result : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="049af-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="049af-106">Input</span></span>

### <a name="xs--littleendian"></a><span data-ttu-id="049af-107">xs: [littleenddian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="049af-107">xs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="049af-108">Erste $n $-Bit-Nummer</span><span class="sxs-lookup"><span data-stu-id="049af-108">First $n$-bit number</span></span>


### <a name="ys--littleendian"></a><span data-ttu-id="049af-109">YS: [littleumdian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="049af-109">ys : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="049af-110">Sekunde $n $-Bit-Zahl</span><span class="sxs-lookup"><span data-stu-id="049af-110">Second $n$-bit number</span></span>


### <a name="result--qubit"></a><span data-ttu-id="049af-111">Ergebnis: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="049af-111">result : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="049af-112">Wird gekippt, wenn $x > y $</span><span class="sxs-lookup"><span data-stu-id="049af-112">Will be flipped if $x > y$</span></span>



## <a name="output--unit"></a><span data-ttu-id="049af-113">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="049af-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

