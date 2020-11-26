---
uid: Microsoft.Quantum.Arithmetic.CompareGTSI
title: Comparegtsi-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: CompareGTSI
qsharp.summary: 'Wrapper for signed integer comparison: `result = xs > ys`.'
ms.openlocfilehash: a0e8ef66f1e1a62d4f6a78364135376810507534
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96223492"
---
# <a name="comparegtsi-operation"></a><span data-ttu-id="53607-102">Comparegtsi-Vorgang</span><span class="sxs-lookup"><span data-stu-id="53607-102">CompareGTSI operation</span></span>

<span data-ttu-id="53607-103">Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="53607-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="53607-104">Paket: [Microsoft. Quantum. Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span><span class="sxs-lookup"><span data-stu-id="53607-104">Package: [Microsoft.Quantum.Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span></span>


<span data-ttu-id="53607-105">Wrapper für ganzzahligen Vergleich mit Vorzeichen: `result = xs > ys` .</span><span class="sxs-lookup"><span data-stu-id="53607-105">Wrapper for signed integer comparison: `result = xs > ys`.</span></span>

```qsharp
operation CompareGTSI (xs : Microsoft.Quantum.Arithmetic.SignedLittleEndian, ys : Microsoft.Quantum.Arithmetic.SignedLittleEndian, result : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="53607-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="53607-106">Input</span></span>

### <a name="xs--signedlittleendian"></a><span data-ttu-id="53607-107">xs: [signedlittleenddian](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)</span><span class="sxs-lookup"><span data-stu-id="53607-107">xs : [SignedLittleEndian](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)</span></span>

<span data-ttu-id="53607-108">Erste $n $-Bit-Nummer</span><span class="sxs-lookup"><span data-stu-id="53607-108">First $n$-bit number</span></span>


### <a name="ys--signedlittleendian"></a><span data-ttu-id="53607-109">YS: [signedlittleenddian](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)</span><span class="sxs-lookup"><span data-stu-id="53607-109">ys : [SignedLittleEndian](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)</span></span>

<span data-ttu-id="53607-110">Sekunde $n $-Bit-Zahl</span><span class="sxs-lookup"><span data-stu-id="53607-110">Second $n$-bit number</span></span>


### <a name="result--qubit"></a><span data-ttu-id="53607-111">Ergebnis: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="53607-111">result : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="53607-112">Wird gekippt, wenn $XS > YS $</span><span class="sxs-lookup"><span data-stu-id="53607-112">Will be flipped if $xs > ys$</span></span>



## <a name="output--unit"></a><span data-ttu-id="53607-113">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="53607-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

