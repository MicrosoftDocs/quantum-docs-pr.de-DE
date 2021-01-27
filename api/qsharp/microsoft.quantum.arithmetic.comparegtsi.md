---
uid: Microsoft.Quantum.Arithmetic.CompareGTSI
title: Comparegtsi-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: CompareGTSI
qsharp.summary: 'Wrapper for signed integer comparison: `result = xs > ys`.'
ms.openlocfilehash: f725bdbaa945a4f87e90fc71930c37642113c21a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846706"
---
# <a name="comparegtsi-operation"></a><span data-ttu-id="1e2e6-102">Comparegtsi-Vorgang</span><span class="sxs-lookup"><span data-stu-id="1e2e6-102">CompareGTSI operation</span></span>

<span data-ttu-id="1e2e6-103">Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="1e2e6-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="1e2e6-104">Paket: [Microsoft. Quantum. Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span><span class="sxs-lookup"><span data-stu-id="1e2e6-104">Package: [Microsoft.Quantum.Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span></span>


<span data-ttu-id="1e2e6-105">Wrapper für ganzzahligen Vergleich mit Vorzeichen: `result = xs > ys` .</span><span class="sxs-lookup"><span data-stu-id="1e2e6-105">Wrapper for signed integer comparison: `result = xs > ys`.</span></span>

```qsharp
operation CompareGTSI (xs : Microsoft.Quantum.Arithmetic.SignedLittleEndian, ys : Microsoft.Quantum.Arithmetic.SignedLittleEndian, result : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="1e2e6-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="1e2e6-106">Input</span></span>

### <a name="xs--signedlittleendian"></a><span data-ttu-id="1e2e6-107">xs: [signedlittleenddian](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)</span><span class="sxs-lookup"><span data-stu-id="1e2e6-107">xs : [SignedLittleEndian](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)</span></span>

<span data-ttu-id="1e2e6-108">Erste $n $-Bit-Nummer</span><span class="sxs-lookup"><span data-stu-id="1e2e6-108">First $n$-bit number</span></span>


### <a name="ys--signedlittleendian"></a><span data-ttu-id="1e2e6-109">YS: [signedlittleenddian](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)</span><span class="sxs-lookup"><span data-stu-id="1e2e6-109">ys : [SignedLittleEndian](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)</span></span>

<span data-ttu-id="1e2e6-110">Sekunde $n $-Bit-Zahl</span><span class="sxs-lookup"><span data-stu-id="1e2e6-110">Second $n$-bit number</span></span>


### <a name="result--qubit"></a><span data-ttu-id="1e2e6-111">Ergebnis: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="1e2e6-111">result : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="1e2e6-112">Wird gekippt, wenn $XS > YS $</span><span class="sxs-lookup"><span data-stu-id="1e2e6-112">Will be flipped if $xs > ys$</span></span>



## <a name="output--unit"></a><span data-ttu-id="1e2e6-113">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="1e2e6-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

