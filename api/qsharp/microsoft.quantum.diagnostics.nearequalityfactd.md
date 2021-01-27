---
uid: Microsoft.Quantum.Diagnostics.NearEqualityFactD
title: Netarequalityfaktd-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: NearEqualityFactD
qsharp.summary: Asserts that a classical floating point value has the expected value up to a small tolerance of 1e-10.
ms.openlocfilehash: d632a7a12c9ebbebfbc7939f2b8a24de8ae1ba2a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98827906"
---
# <a name="nearequalityfactd-function"></a><span data-ttu-id="e09f3-102">Netarequalityfaktd-Funktion</span><span class="sxs-lookup"><span data-stu-id="e09f3-102">NearEqualityFactD function</span></span>

<span data-ttu-id="e09f3-103">Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="e09f3-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="e09f3-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="e09f3-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="e09f3-105">Bestätigt, dass ein klassischer Gleit Komma Wert den erwarteten Wert bis zu einer kleinen Toleranz von 1E-10 aufweist.</span><span class="sxs-lookup"><span data-stu-id="e09f3-105">Asserts that a classical floating point value has the expected value up to a small tolerance of 1e-10.</span></span>

```qsharp
function NearEqualityFactD (actual : Double, expected : Double) : Unit
```


## <a name="input"></a><span data-ttu-id="e09f3-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e09f3-106">Input</span></span>

### <a name="actual--double"></a><span data-ttu-id="e09f3-107">tatsächlicher Wert: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="e09f3-107">actual : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="e09f3-108">Die Zahl, die geprüft werden soll.</span><span class="sxs-lookup"><span data-stu-id="e09f3-108">The number to be checked.</span></span>


### <a name="expected--double"></a><span data-ttu-id="e09f3-109">erwartet: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="e09f3-109">expected : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="e09f3-110">Der erwartete Wert.</span><span class="sxs-lookup"><span data-stu-id="e09f3-110">The expected value.</span></span>



## <a name="output--unit"></a><span data-ttu-id="e09f3-111">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="e09f3-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="e09f3-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e09f3-112">Remarks</span></span>

<span data-ttu-id="e09f3-113">Dies entspricht <xref:microsoft.quantum.diagnostics.equalitywithintolerancefact> der hart codierten Toleranz von $10 ^ {-10} $.</span><span class="sxs-lookup"><span data-stu-id="e09f3-113">This is equivalent to <xref:microsoft.quantum.diagnostics.equalitywithintolerancefact> with hardcoded tolerance of $10^{-10}$.</span></span>