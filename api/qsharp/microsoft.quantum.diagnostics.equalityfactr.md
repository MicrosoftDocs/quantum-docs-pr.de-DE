---
uid: Microsoft.Quantum.Diagnostics.EqualityFactR
title: Equalityfaktr-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: EqualityFactR
qsharp.summary: Asserts that a classical Result variable has the expected value.
ms.openlocfilehash: 166dff211d6db9da5d39c607af1924ffd6d276dd
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96201766"
---
# <a name="equalityfactr-function"></a><span data-ttu-id="6cbd5-102">Equalityfaktr-Funktion</span><span class="sxs-lookup"><span data-stu-id="6cbd5-102">EqualityFactR function</span></span>

<span data-ttu-id="6cbd5-103">Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="6cbd5-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="6cbd5-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="6cbd5-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="6cbd5-105">Bestätigt, dass eine klassische Ergebnisvariable über den erwarteten Wert verfügt.</span><span class="sxs-lookup"><span data-stu-id="6cbd5-105">Asserts that a classical Result variable has the expected value.</span></span>

```qsharp
function EqualityFactR (actual : Result, expected : Result, message : String) : Unit
```


## <a name="input"></a><span data-ttu-id="6cbd5-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6cbd5-106">Input</span></span>

### <a name="actual--__invalidresult__"></a><span data-ttu-id="6cbd5-107">tatsächlicher Wert: __ungültig <Result>__</span><span class="sxs-lookup"><span data-stu-id="6cbd5-107">actual : __invalid<Result>__</span></span>

<span data-ttu-id="6cbd5-108">Die zu überprüfende Variable.</span><span class="sxs-lookup"><span data-stu-id="6cbd5-108">The variable to be checked.</span></span>


### <a name="expected--__invalidresult__"></a><span data-ttu-id="6cbd5-109">erwartet: __ungültig <Result>__</span><span class="sxs-lookup"><span data-stu-id="6cbd5-109">expected : __invalid<Result>__</span></span>

<span data-ttu-id="6cbd5-110">Der erwartete Wert.</span><span class="sxs-lookup"><span data-stu-id="6cbd5-110">The expected value.</span></span>


### <a name="message--string"></a><span data-ttu-id="6cbd5-111">Message: [Zeichenfolge](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="6cbd5-111">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="6cbd5-112">Fehlermeldungs Zeichenfolge, die verwendet wird, wenn die-Assertion ausgelöst wird</span><span class="sxs-lookup"><span data-stu-id="6cbd5-112">Failure message string to be used when the assertion is triggered.</span></span>



## <a name="output--unit"></a><span data-ttu-id="6cbd5-113">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="6cbd5-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

