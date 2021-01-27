---
uid: Microsoft.Quantum.Diagnostics.EqualityWithinToleranceFact
title: Equalitywithintolerancefact-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: EqualityWithinToleranceFact
qsharp.summary: Represents the claim that a classical floating point value has the expected value up to a given absolute tolerance.
ms.openlocfilehash: ab7e43d951bf741926b15f27f94d176e88609d4a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98828747"
---
# <a name="equalitywithintolerancefact-function"></a><span data-ttu-id="8315b-102">Equalitywithintolerancefact-Funktion</span><span class="sxs-lookup"><span data-stu-id="8315b-102">EqualityWithinToleranceFact function</span></span>

<span data-ttu-id="8315b-103">Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="8315b-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="8315b-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="8315b-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="8315b-105">Stellt den Anspruch dar, dass ein klassischer Gleit Komma Wert den erwarteten Wert bis zu einer bestimmten absoluten Toleranz aufweist.</span><span class="sxs-lookup"><span data-stu-id="8315b-105">Represents the claim that a classical floating point value has the expected value up to a given absolute tolerance.</span></span>

```qsharp
function EqualityWithinToleranceFact (actual : Double, expected : Double, tolerance : Double) : Unit
```


## <a name="input"></a><span data-ttu-id="8315b-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8315b-106">Input</span></span>

### <a name="actual--double"></a><span data-ttu-id="8315b-107">tatsächlicher Wert: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="8315b-107">actual : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="8315b-108">Die Zahl, die geprüft werden soll.</span><span class="sxs-lookup"><span data-stu-id="8315b-108">The number to be checked.</span></span>


### <a name="expected--double"></a><span data-ttu-id="8315b-109">erwartet: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="8315b-109">expected : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="8315b-110">Der erwartete Wert.</span><span class="sxs-lookup"><span data-stu-id="8315b-110">The expected value.</span></span>


### <a name="tolerance--double"></a><span data-ttu-id="8315b-111">Toleranz: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="8315b-111">tolerance : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="8315b-112">Absolute Toleranz für den Unterschied zwischen tatsächlichem und erwartetem Verhalten.</span><span class="sxs-lookup"><span data-stu-id="8315b-112">Absolute tolerance on the difference between actual and expected.</span></span>



## <a name="output--unit"></a><span data-ttu-id="8315b-113">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="8315b-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

