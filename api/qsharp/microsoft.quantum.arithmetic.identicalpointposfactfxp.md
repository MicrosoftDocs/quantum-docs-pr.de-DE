---
uid: Microsoft.Quantum.Arithmetic.IdenticalPointPosFactFxP
title: Identicalpointposfaktfxp-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: IdenticalPointPosFactFxP
qsharp.summary: Assert that all fixed-point numbers in the provided array have identical point positions when counting from the least- significant bit. I.e., number of bits minus point position must be constant for all fixed-point numbers in the array.
ms.openlocfilehash: 7212f918e1d0ee86b12b85caa6e0c27bc2cebe58
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846617"
---
# <a name="identicalpointposfactfxp-function"></a><span data-ttu-id="adcfa-102">Identicalpointposfaktfxp-Funktion</span><span class="sxs-lookup"><span data-stu-id="adcfa-102">IdenticalPointPosFactFxP function</span></span>

<span data-ttu-id="adcfa-103">Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="adcfa-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="adcfa-104">Paket: [Microsoft. Quantum. Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span><span class="sxs-lookup"><span data-stu-id="adcfa-104">Package: [Microsoft.Quantum.Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span></span>


<span data-ttu-id="adcfa-105">Bestätigen Sie, dass alle fest Komma Zahlen im angegebenen Array identische Punktpositionen aufweisen, wenn Sie vom unwichtigsten Bit gezählt werden.</span><span class="sxs-lookup"><span data-stu-id="adcfa-105">Assert that all fixed-point numbers in the provided array have identical point positions when counting from the least- significant bit.</span></span> <span data-ttu-id="adcfa-106">Dies bedeutet, dass die Anzahl der Bits, die Minuspunkt Positionen aufweisen, für alle Festkomma Zahlen im Array konstant sein muss.</span><span class="sxs-lookup"><span data-stu-id="adcfa-106">I.e., number of bits minus point position must be constant for all fixed-point numbers in the array.</span></span>

```qsharp
function IdenticalPointPosFactFxP (fixedPoints : Microsoft.Quantum.Arithmetic.FixedPoint[]) : Unit
```


## <a name="input"></a><span data-ttu-id="adcfa-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="adcfa-107">Input</span></span>

### <a name="fixedpoints--fixedpoint"></a><span data-ttu-id="adcfa-108">fixedpoints: [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)[]</span><span class="sxs-lookup"><span data-stu-id="adcfa-108">fixedPoints : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)[]</span></span>

<span data-ttu-id="adcfa-109">Array von Quantum-fixpunktzahlen, die auf Kompatibilität geprüft werden (mithilfe von Assertionen).</span><span class="sxs-lookup"><span data-stu-id="adcfa-109">Array of quantum fixed-point numbers that will be checked for compatibility (using assertions).</span></span>



## <a name="output--unit"></a><span data-ttu-id="adcfa-110">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="adcfa-110">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

