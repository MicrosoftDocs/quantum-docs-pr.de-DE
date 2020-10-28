---
uid: Microsoft.Quantum.Chemistry.JordanWigner.OptimizedBEGeneratorSystem
title: Benutzerdefinierter optimizedbegeneratorsystem-Typ
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: OptimizedBEGeneratorSystem
qsharp.summary: Function that returns `OptimizedBETermIndex` data for term `n` given an integer `n`, together with the number of terms in the first `Int` and the sum of absolute-values of all term coefficients in the `Double`.
ms.openlocfilehash: 06d13a8a64a3c572821ec97f8776d6f1dbe4a4ce
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703169"
---
# <a name="optimizedbegeneratorsystem-user-defined-type"></a><span data-ttu-id="43bf6-102">Benutzerdefinierter optimizedbegeneratorsystem-Typ</span><span class="sxs-lookup"><span data-stu-id="43bf6-102">OptimizedBEGeneratorSystem user defined type</span></span>

<span data-ttu-id="43bf6-103">Namespace: [Microsoft. Quantum. Chemistry. jordanwigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="43bf6-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="43bf6-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="43bf6-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="43bf6-105">Eine Funktion, die Daten für den Begriff "Integer" zurückgibt `OptimizedBETermIndex` `n` `n` , und zwar zusammen mit der Anzahl der Begriffe in der ersten `Int` und der Summe der absoluten Werte aller Begriffs Koeffizienten in `Double` .</span><span class="sxs-lookup"><span data-stu-id="43bf6-105">Function that returns `OptimizedBETermIndex` data for term `n` given an integer `n`, together with the number of terms in the first `Int` and the sum of absolute-values of all term coefficients in the `Double`.</span></span>

```qsharp

newtype OptimizedBEGeneratorSystem = (Int, Double, (Int -> Microsoft.Quantum.Chemistry.JordanWigner.OptimizedBETermIndex));
```

