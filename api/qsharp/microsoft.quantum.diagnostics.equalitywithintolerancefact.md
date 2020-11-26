---
uid: Microsoft.Quantum.Diagnostics.EqualityWithinToleranceFact
title: Equalitywithintolerancefact-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: EqualityWithinToleranceFact
qsharp.summary: Represents the claim that a classical floating point value has the expected value up to a given absolute tolerance.
ms.openlocfilehash: 6ada2632974fddd6dd0fd8e4e6ab0866e4f29524
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96201715"
---
# <a name="equalitywithintolerancefact-function"></a><span data-ttu-id="031b4-102">Equalitywithintolerancefact-Funktion</span><span class="sxs-lookup"><span data-stu-id="031b4-102">EqualityWithinToleranceFact function</span></span>

<span data-ttu-id="031b4-103">Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="031b4-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="031b4-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="031b4-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="031b4-105">Stellt den Anspruch dar, dass ein klassischer Gleit Komma Wert den erwarteten Wert bis zu einer bestimmten absoluten Toleranz aufweist.</span><span class="sxs-lookup"><span data-stu-id="031b4-105">Represents the claim that a classical floating point value has the expected value up to a given absolute tolerance.</span></span>

```qsharp
function EqualityWithinToleranceFact (actual : Double, expected : Double, tolerance : Double) : Unit
```


## <a name="input"></a><span data-ttu-id="031b4-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="031b4-106">Input</span></span>

### <a name="actual--double"></a><span data-ttu-id="031b4-107">tatsächlicher Wert: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="031b4-107">actual : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="031b4-108">Die Zahl, die geprüft werden soll.</span><span class="sxs-lookup"><span data-stu-id="031b4-108">The number to be checked.</span></span>


### <a name="expected--double"></a><span data-ttu-id="031b4-109">erwartet: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="031b4-109">expected : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="031b4-110">Der erwartete Wert.</span><span class="sxs-lookup"><span data-stu-id="031b4-110">The expected value.</span></span>


### <a name="tolerance--double"></a><span data-ttu-id="031b4-111">Toleranz: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="031b4-111">tolerance : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="031b4-112">Absolute Toleranz für den Unterschied zwischen tatsächlichem und erwartetem Verhalten.</span><span class="sxs-lookup"><span data-stu-id="031b4-112">Absolute tolerance on the difference between actual and expected.</span></span>



## <a name="output--unit"></a><span data-ttu-id="031b4-113">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="031b4-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

