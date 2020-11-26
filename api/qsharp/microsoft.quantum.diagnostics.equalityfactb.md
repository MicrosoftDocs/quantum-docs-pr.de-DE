---
uid: Microsoft.Quantum.Diagnostics.EqualityFactB
title: Equalityfaktb-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: EqualityFactB
qsharp.summary: Asserts that a classical Bool variable has the expected value.
ms.openlocfilehash: a87d6690e701eb1530be3134d24884a8c19357e9
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96201919"
---
# <a name="equalityfactb-function"></a><span data-ttu-id="4e03e-102">Equalityfaktb-Funktion</span><span class="sxs-lookup"><span data-stu-id="4e03e-102">EqualityFactB function</span></span>

<span data-ttu-id="4e03e-103">Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="4e03e-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="4e03e-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="4e03e-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="4e03e-105">Bestätigt, dass eine klassische boolesche Variable über den erwarteten Wert verfügt.</span><span class="sxs-lookup"><span data-stu-id="4e03e-105">Asserts that a classical Bool variable has the expected value.</span></span>

```qsharp
function EqualityFactB (actual : Bool, expected : Bool, message : String) : Unit
```


## <a name="input"></a><span data-ttu-id="4e03e-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="4e03e-106">Input</span></span>

### <a name="actual--bool"></a><span data-ttu-id="4e03e-107">tatsächlicher Wert: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="4e03e-107">actual : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="4e03e-108">Die zu überprüfende Variable.</span><span class="sxs-lookup"><span data-stu-id="4e03e-108">The variable to be checked.</span></span>


### <a name="expected--bool"></a><span data-ttu-id="4e03e-109">erwartet: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="4e03e-109">expected : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="4e03e-110">Der erwartete Wert.</span><span class="sxs-lookup"><span data-stu-id="4e03e-110">The expected value.</span></span>


### <a name="message--string"></a><span data-ttu-id="4e03e-111">Message: [Zeichenfolge](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="4e03e-111">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="4e03e-112">Fehlermeldungs Zeichenfolge, die verwendet wird, wenn die-Assertion ausgelöst wird</span><span class="sxs-lookup"><span data-stu-id="4e03e-112">Failure message string to be used when the assertion is triggered.</span></span>



## <a name="output--unit"></a><span data-ttu-id="4e03e-113">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="4e03e-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

