---
uid: Microsoft.Quantum.Diagnostics.NearEqualityFactD
title: Netarequalityfaktd-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: NearEqualityFactD
qsharp.summary: Asserts that a classical floating point value has the expected value up to a small tolerance of 1e-10.
ms.openlocfilehash: 5acfe5043342fd88276910a9fd0347f7d2f6960f
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96201511"
---
# <a name="nearequalityfactd-function"></a><span data-ttu-id="63def-102">Netarequalityfaktd-Funktion</span><span class="sxs-lookup"><span data-stu-id="63def-102">NearEqualityFactD function</span></span>

<span data-ttu-id="63def-103">Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="63def-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="63def-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="63def-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="63def-105">Bestätigt, dass ein klassischer Gleit Komma Wert den erwarteten Wert bis zu einer kleinen Toleranz von 1E-10 aufweist.</span><span class="sxs-lookup"><span data-stu-id="63def-105">Asserts that a classical floating point value has the expected value up to a small tolerance of 1e-10.</span></span>

```qsharp
function NearEqualityFactD (actual : Double, expected : Double) : Unit
```


## <a name="input"></a><span data-ttu-id="63def-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="63def-106">Input</span></span>

### <a name="actual--double"></a><span data-ttu-id="63def-107">tatsächlicher Wert: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="63def-107">actual : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="63def-108">Die Zahl, die geprüft werden soll.</span><span class="sxs-lookup"><span data-stu-id="63def-108">The number to be checked.</span></span>


### <a name="expected--double"></a><span data-ttu-id="63def-109">erwartet: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="63def-109">expected : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="63def-110">Der erwartete Wert.</span><span class="sxs-lookup"><span data-stu-id="63def-110">The expected value.</span></span>



## <a name="output--unit"></a><span data-ttu-id="63def-111">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="63def-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="63def-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="63def-112">Remarks</span></span>

<span data-ttu-id="63def-113">Dies entspricht <xref:microsoft.quantum.diagnostics.equalitywithintolerancefact> der hart codierten Toleranz von $10 ^ {-10} $.</span><span class="sxs-lookup"><span data-stu-id="63def-113">This is equivalent to <xref:microsoft.quantum.diagnostics.equalitywithintolerancefact> with hardcoded tolerance of $10^{-10}$.</span></span>