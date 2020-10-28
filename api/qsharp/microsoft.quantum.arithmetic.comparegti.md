---
uid: Microsoft.Quantum.Arithmetic.CompareGTI
title: Comparegti-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: CompareGTI
qsharp.summary: 'Wrapper for integer comparison: `result = x > y`.'
ms.openlocfilehash: c60c2827060f4ef223ebaf80ccdef09faaf56098
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707386"
---
# <a name="comparegti-operation"></a><span data-ttu-id="25629-102">Comparegti-Vorgang</span><span class="sxs-lookup"><span data-stu-id="25629-102">CompareGTI operation</span></span>

<span data-ttu-id="25629-103">Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="25629-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="25629-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="25629-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="25629-105">Wrapper für ganzzahligen Vergleich: `result = x > y` .</span><span class="sxs-lookup"><span data-stu-id="25629-105">Wrapper for integer comparison: `result = x > y`.</span></span>

```qsharp
operation CompareGTI (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian, result : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="25629-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="25629-106">Input</span></span>

### <a name="xs--littleendian"></a><span data-ttu-id="25629-107">xs: [littleenddian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="25629-107">xs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="25629-108">Erste $n $-Bit-Nummer</span><span class="sxs-lookup"><span data-stu-id="25629-108">First $n$-bit number</span></span>


### <a name="ys--littleendian"></a><span data-ttu-id="25629-109">YS: [littleumdian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="25629-109">ys : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="25629-110">Sekunde $n $-Bit-Zahl</span><span class="sxs-lookup"><span data-stu-id="25629-110">Second $n$-bit number</span></span>


### <a name="result--qubit"></a><span data-ttu-id="25629-111">Ergebnis: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="25629-111">result : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="25629-112">Wird gekippt, wenn $x > y $</span><span class="sxs-lookup"><span data-stu-id="25629-112">Will be flipped if $x > y$</span></span>



## <a name="output--unit"></a><span data-ttu-id="25629-113">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="25629-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

