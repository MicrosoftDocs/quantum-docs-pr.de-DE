---
uid: Microsoft.Quantum.Arithmetic.IdenticalPointPosFactFxP
title: Identicalpointposfaktfxp-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: IdenticalPointPosFactFxP
qsharp.summary: Assert that all fixed-point numbers in the provided array have identical point positions when counting from the least- significant bit. I.e., number of bits minus point position must be constant for all fixed-point numbers in the array.
ms.openlocfilehash: 907e270e1c3710fb346044ad7757171c6d5f568d
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96223050"
---
# <a name="identicalpointposfactfxp-function"></a><span data-ttu-id="7d533-102">Identicalpointposfaktfxp-Funktion</span><span class="sxs-lookup"><span data-stu-id="7d533-102">IdenticalPointPosFactFxP function</span></span>

<span data-ttu-id="7d533-103">Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="7d533-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="7d533-104">Paket: [Microsoft. Quantum. Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span><span class="sxs-lookup"><span data-stu-id="7d533-104">Package: [Microsoft.Quantum.Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span></span>


<span data-ttu-id="7d533-105">Bestätigen Sie, dass alle fest Komma Zahlen im angegebenen Array identische Punktpositionen aufweisen, wenn Sie vom unwichtigsten Bit gezählt werden.</span><span class="sxs-lookup"><span data-stu-id="7d533-105">Assert that all fixed-point numbers in the provided array have identical point positions when counting from the least- significant bit.</span></span> <span data-ttu-id="7d533-106">Dies bedeutet, dass die Anzahl der Bits, die Minuspunkt Positionen aufweisen, für alle Festkomma Zahlen im Array konstant sein muss.</span><span class="sxs-lookup"><span data-stu-id="7d533-106">I.e., number of bits minus point position must be constant for all fixed-point numbers in the array.</span></span>

```qsharp
function IdenticalPointPosFactFxP (fixedPoints : Microsoft.Quantum.Arithmetic.FixedPoint[]) : Unit
```


## <a name="input"></a><span data-ttu-id="7d533-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="7d533-107">Input</span></span>

### <a name="fixedpoints--fixedpoint"></a><span data-ttu-id="7d533-108">fixedpoints: [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)[]</span><span class="sxs-lookup"><span data-stu-id="7d533-108">fixedPoints : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)[]</span></span>

<span data-ttu-id="7d533-109">Array von Quantum-fixpunktzahlen, die auf Kompatibilität geprüft werden (mithilfe von Assertionen).</span><span class="sxs-lookup"><span data-stu-id="7d533-109">Array of quantum fixed-point numbers that will be checked for compatibility (using assertions).</span></span>



## <a name="output--unit"></a><span data-ttu-id="7d533-110">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="7d533-110">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

