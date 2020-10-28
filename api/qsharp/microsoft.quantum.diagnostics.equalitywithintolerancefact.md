---
uid: Microsoft.Quantum.Diagnostics.EqualityWithinToleranceFact
title: Equalitywithintolerancefact-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: EqualityWithinToleranceFact
qsharp.summary: Represents the claim that a classical floating point value has the expected value up to a given absolute tolerance.
ms.openlocfilehash: de15a32d5b38c5ab8c681d2c052669a48cf676cc
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702659"
---
# <a name="equalitywithintolerancefact-function"></a><span data-ttu-id="76eb4-102">Equalitywithintolerancefact-Funktion</span><span class="sxs-lookup"><span data-stu-id="76eb4-102">EqualityWithinToleranceFact function</span></span>

<span data-ttu-id="76eb4-103">Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="76eb4-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="76eb4-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="76eb4-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="76eb4-105">Stellt den Anspruch dar, dass ein klassischer Gleit Komma Wert den erwarteten Wert bis zu einer bestimmten absoluten Toleranz aufweist.</span><span class="sxs-lookup"><span data-stu-id="76eb4-105">Represents the claim that a classical floating point value has the expected value up to a given absolute tolerance.</span></span>

```qsharp
function EqualityWithinToleranceFact (actual : Double, expected : Double, tolerance : Double) : Unit
```


## <a name="input"></a><span data-ttu-id="76eb4-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="76eb4-106">Input</span></span>

### <a name="actual--double"></a><span data-ttu-id="76eb4-107">tatsächlicher Wert: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="76eb4-107">actual : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="76eb4-108">Die Zahl, die geprüft werden soll.</span><span class="sxs-lookup"><span data-stu-id="76eb4-108">The number to be checked.</span></span>


### <a name="expected--double"></a><span data-ttu-id="76eb4-109">erwartet: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="76eb4-109">expected : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="76eb4-110">Der erwartete Wert.</span><span class="sxs-lookup"><span data-stu-id="76eb4-110">The expected value.</span></span>


### <a name="tolerance--double"></a><span data-ttu-id="76eb4-111">Toleranz: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="76eb4-111">tolerance : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="76eb4-112">Absolute Toleranz für den Unterschied zwischen tatsächlichem und erwartetem Verhalten.</span><span class="sxs-lookup"><span data-stu-id="76eb4-112">Absolute tolerance on the difference between actual and expected.</span></span>



## <a name="output--unit"></a><span data-ttu-id="76eb4-113">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="76eb4-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

