---
uid: Microsoft.Quantum.Arithmetic.CompareGTI
title: Comparegti-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: CompareGTI
qsharp.summary: 'Wrapper for integer comparison: `result = x > y`.'
ms.openlocfilehash: b6e82eb7e9c068eff5bb320bb797a8fb0f8f921b
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96223475"
---
# <a name="comparegti-operation"></a><span data-ttu-id="56d51-102">Comparegti-Vorgang</span><span class="sxs-lookup"><span data-stu-id="56d51-102">CompareGTI operation</span></span>

<span data-ttu-id="56d51-103">Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="56d51-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="56d51-104">Paket: [Microsoft. Quantum. Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span><span class="sxs-lookup"><span data-stu-id="56d51-104">Package: [Microsoft.Quantum.Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span></span>


<span data-ttu-id="56d51-105">Wrapper für ganzzahligen Vergleich: `result = x > y` .</span><span class="sxs-lookup"><span data-stu-id="56d51-105">Wrapper for integer comparison: `result = x > y`.</span></span>

```qsharp
operation CompareGTI (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian, result : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="56d51-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="56d51-106">Input</span></span>

### <a name="xs--littleendian"></a><span data-ttu-id="56d51-107">xs: [littleenddian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="56d51-107">xs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="56d51-108">Erste $n $-Bit-Nummer</span><span class="sxs-lookup"><span data-stu-id="56d51-108">First $n$-bit number</span></span>


### <a name="ys--littleendian"></a><span data-ttu-id="56d51-109">YS: [littleumdian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="56d51-109">ys : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="56d51-110">Sekunde $n $-Bit-Zahl</span><span class="sxs-lookup"><span data-stu-id="56d51-110">Second $n$-bit number</span></span>


### <a name="result--qubit"></a><span data-ttu-id="56d51-111">Ergebnis: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="56d51-111">result : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="56d51-112">Wird gekippt, wenn $x > y $</span><span class="sxs-lookup"><span data-stu-id="56d51-112">Will be flipped if $x > y$</span></span>



## <a name="output--unit"></a><span data-ttu-id="56d51-113">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="56d51-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

