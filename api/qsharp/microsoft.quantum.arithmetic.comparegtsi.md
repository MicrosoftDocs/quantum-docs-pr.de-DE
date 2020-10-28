---
uid: Microsoft.Quantum.Arithmetic.CompareGTSI
title: Comparegtsi-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: CompareGTSI
qsharp.summary: 'Wrapper for signed integer comparison: `result = xs > ys`.'
ms.openlocfilehash: 735ae21168d8efb3e626a8f1ea36e97f5cdf8760
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707383"
---
# <a name="comparegtsi-operation"></a><span data-ttu-id="6f1cf-102">Comparegtsi-Vorgang</span><span class="sxs-lookup"><span data-stu-id="6f1cf-102">CompareGTSI operation</span></span>

<span data-ttu-id="6f1cf-103">Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="6f1cf-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="6f1cf-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="6f1cf-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="6f1cf-105">Wrapper für ganzzahligen Vergleich mit Vorzeichen: `result = xs > ys` .</span><span class="sxs-lookup"><span data-stu-id="6f1cf-105">Wrapper for signed integer comparison: `result = xs > ys`.</span></span>

```qsharp
operation CompareGTSI (xs : Microsoft.Quantum.Arithmetic.SignedLittleEndian, ys : Microsoft.Quantum.Arithmetic.SignedLittleEndian, result : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="6f1cf-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6f1cf-106">Input</span></span>

### <a name="xs--signedlittleendian"></a><span data-ttu-id="6f1cf-107">xs: [signedlittleenddian](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)</span><span class="sxs-lookup"><span data-stu-id="6f1cf-107">xs : [SignedLittleEndian](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)</span></span>

<span data-ttu-id="6f1cf-108">Erste $n $-Bit-Nummer</span><span class="sxs-lookup"><span data-stu-id="6f1cf-108">First $n$-bit number</span></span>


### <a name="ys--signedlittleendian"></a><span data-ttu-id="6f1cf-109">YS: [signedlittleenddian](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)</span><span class="sxs-lookup"><span data-stu-id="6f1cf-109">ys : [SignedLittleEndian](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)</span></span>

<span data-ttu-id="6f1cf-110">Sekunde $n $-Bit-Zahl</span><span class="sxs-lookup"><span data-stu-id="6f1cf-110">Second $n$-bit number</span></span>


### <a name="result--qubit"></a><span data-ttu-id="6f1cf-111">Ergebnis: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="6f1cf-111">result : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="6f1cf-112">Wird gekippt, wenn $XS > YS $</span><span class="sxs-lookup"><span data-stu-id="6f1cf-112">Will be flipped if $xs > ys$</span></span>



## <a name="output--unit"></a><span data-ttu-id="6f1cf-113">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="6f1cf-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

