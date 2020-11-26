---
uid: Microsoft.Quantum.Diagnostics.EqualityFactL
title: Equalityfaktl-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: EqualityFactL
qsharp.summary: Asserts that a classical BigInt variable has the expected value.
ms.openlocfilehash: 2aaabf39d6ce49952466a877685776490ef438ad
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96201800"
---
# <a name="equalityfactl-function"></a><span data-ttu-id="26ef7-102">Equalityfaktl-Funktion</span><span class="sxs-lookup"><span data-stu-id="26ef7-102">EqualityFactL function</span></span>

<span data-ttu-id="26ef7-103">Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="26ef7-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="26ef7-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="26ef7-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="26ef7-105">Bestätigt, dass eine klassische bigint-Variable über den erwarteten Wert verfügt.</span><span class="sxs-lookup"><span data-stu-id="26ef7-105">Asserts that a classical BigInt variable has the expected value.</span></span>

```qsharp
function EqualityFactL (actual : BigInt, expected : BigInt, message : String) : Unit
```


## <a name="input"></a><span data-ttu-id="26ef7-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="26ef7-106">Input</span></span>

### <a name="actual--bigint"></a><span data-ttu-id="26ef7-107">tatsächlicher Wert: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="26ef7-107">actual : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="26ef7-108">Die Zahl, die geprüft werden soll.</span><span class="sxs-lookup"><span data-stu-id="26ef7-108">The number to be checked.</span></span>


### <a name="expected--bigint"></a><span data-ttu-id="26ef7-109">erwartet: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="26ef7-109">expected : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="26ef7-110">Der erwartete Wert.</span><span class="sxs-lookup"><span data-stu-id="26ef7-110">The expected value.</span></span>


### <a name="message--string"></a><span data-ttu-id="26ef7-111">Message: [Zeichenfolge](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="26ef7-111">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="26ef7-112">Fehlermeldungs Zeichenfolge, die verwendet wird, wenn die-Assertion ausgelöst wird</span><span class="sxs-lookup"><span data-stu-id="26ef7-112">Failure message string to be used when the assertion is triggered.</span></span>



## <a name="output--unit"></a><span data-ttu-id="26ef7-113">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="26ef7-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

