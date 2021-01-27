---
uid: Microsoft.Quantum.Diagnostics.EqualityFactR
title: Equalityfaktr-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: EqualityFactR
qsharp.summary: Asserts that a classical Result variable has the expected value.
ms.openlocfilehash: 86d2ddff79f0bca7badd95a2fe2156c558fa7f86
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853327"
---
# <a name="equalityfactr-function"></a><span data-ttu-id="7e189-102">Equalityfaktr-Funktion</span><span class="sxs-lookup"><span data-stu-id="7e189-102">EqualityFactR function</span></span>

<span data-ttu-id="7e189-103">Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="7e189-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="7e189-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="7e189-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="7e189-105">Bestätigt, dass eine klassische Ergebnisvariable über den erwarteten Wert verfügt.</span><span class="sxs-lookup"><span data-stu-id="7e189-105">Asserts that a classical Result variable has the expected value.</span></span>

```qsharp
function EqualityFactR (actual : Result, expected : Result, message : String) : Unit
```


## <a name="input"></a><span data-ttu-id="7e189-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="7e189-106">Input</span></span>

### <a name="actual--__invalidresult__"></a><span data-ttu-id="7e189-107">tatsächlicher Wert: __ungültig <Result>__</span><span class="sxs-lookup"><span data-stu-id="7e189-107">actual : __invalid<Result>__</span></span>

<span data-ttu-id="7e189-108">Die zu überprüfende Variable.</span><span class="sxs-lookup"><span data-stu-id="7e189-108">The variable to be checked.</span></span>


### <a name="expected--__invalidresult__"></a><span data-ttu-id="7e189-109">erwartet: __ungültig <Result>__</span><span class="sxs-lookup"><span data-stu-id="7e189-109">expected : __invalid<Result>__</span></span>

<span data-ttu-id="7e189-110">Der erwartete Wert.</span><span class="sxs-lookup"><span data-stu-id="7e189-110">The expected value.</span></span>


### <a name="message--string"></a><span data-ttu-id="7e189-111">Message: [Zeichenfolge](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="7e189-111">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="7e189-112">Fehlermeldungs Zeichenfolge, die verwendet wird, wenn die-Assertion ausgelöst wird</span><span class="sxs-lookup"><span data-stu-id="7e189-112">Failure message string to be used when the assertion is triggered.</span></span>



## <a name="output--unit"></a><span data-ttu-id="7e189-113">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="7e189-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

