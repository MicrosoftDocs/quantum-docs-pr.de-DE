---
uid: Microsoft.Quantum.Diagnostics.NearEqualityFactD
title: Netarequalityfaktd-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: NearEqualityFactD
qsharp.summary: Asserts that a classical floating point value has the expected value up to a small tolerance of 1e-10.
ms.openlocfilehash: 5b55f515b27667071218a3f604ef703a6a15206d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702617"
---
# <a name="nearequalityfactd-function"></a><span data-ttu-id="bceab-102">Netarequalityfaktd-Funktion</span><span class="sxs-lookup"><span data-stu-id="bceab-102">NearEqualityFactD function</span></span>

<span data-ttu-id="bceab-103">Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="bceab-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="bceab-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="bceab-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="bceab-105">Bestätigt, dass ein klassischer Gleit Komma Wert den erwarteten Wert bis zu einer kleinen Toleranz von 1E-10 aufweist.</span><span class="sxs-lookup"><span data-stu-id="bceab-105">Asserts that a classical floating point value has the expected value up to a small tolerance of 1e-10.</span></span>

```qsharp
function NearEqualityFactD (actual : Double, expected : Double) : Unit
```


## <a name="input"></a><span data-ttu-id="bceab-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="bceab-106">Input</span></span>

### <a name="actual--double"></a><span data-ttu-id="bceab-107">tatsächlicher Wert: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="bceab-107">actual : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="bceab-108">Die Zahl, die geprüft werden soll.</span><span class="sxs-lookup"><span data-stu-id="bceab-108">The number to be checked.</span></span>


### <a name="expected--double"></a><span data-ttu-id="bceab-109">erwartet: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="bceab-109">expected : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="bceab-110">Der erwartete Wert.</span><span class="sxs-lookup"><span data-stu-id="bceab-110">The expected value.</span></span>



## <a name="output--unit"></a><span data-ttu-id="bceab-111">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="bceab-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="bceab-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="bceab-112">Remarks</span></span>

<span data-ttu-id="bceab-113">Dies entspricht <xref:microsoft.quantum.diagnostics.equalitywithintolerancefact> der hart codierten Toleranz von $10 ^ {-10} $.</span><span class="sxs-lookup"><span data-stu-id="bceab-113">This is equivalent to <xref:microsoft.quantum.diagnostics.equalitywithintolerancefact> with hardcoded tolerance of $10^{-10}$.</span></span>