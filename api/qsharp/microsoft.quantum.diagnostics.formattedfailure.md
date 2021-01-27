---
uid: Microsoft.Quantum.Diagnostics.FormattedFailure
title: Formattedfailure-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: FormattedFailure
qsharp.summary: Internal function used to fail with meaningful error messages.
ms.openlocfilehash: 6b1202c8897d67e3089a88a0855c8008b3a8c2ba
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98828274"
---
# <a name="formattedfailure-function"></a><span data-ttu-id="d99c0-102">Formattedfailure-Funktion</span><span class="sxs-lookup"><span data-stu-id="d99c0-102">FormattedFailure function</span></span>

<span data-ttu-id="d99c0-103">Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="d99c0-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="d99c0-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="d99c0-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="d99c0-105">Interne Funktion, die verwendet wird, um mit aussagekräftigen Fehlermeldungen fehlschlägt</span><span class="sxs-lookup"><span data-stu-id="d99c0-105">Internal function used to fail with meaningful error messages.</span></span>

```qsharp
function FormattedFailure<'T> (actual : 'T, expected : 'T, message : String) : Unit
```


## <a name="input"></a><span data-ttu-id="d99c0-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d99c0-106">Input</span></span>

### <a name="actual--t"></a><span data-ttu-id="d99c0-107">tatsächlicher Wert: 't</span><span class="sxs-lookup"><span data-stu-id="d99c0-107">actual : 'T</span></span>




### <a name="expected--t"></a><span data-ttu-id="d99c0-108">erwartet: 't</span><span class="sxs-lookup"><span data-stu-id="d99c0-108">expected : 'T</span></span>




### <a name="message--string"></a><span data-ttu-id="d99c0-109">Message: [Zeichenfolge](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="d99c0-109">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>





## <a name="output--unit"></a><span data-ttu-id="d99c0-110">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="d99c0-110">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="d99c0-111">Typparameter</span><span class="sxs-lookup"><span data-stu-id="d99c0-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="d99c0-112">GIF</span><span class="sxs-lookup"><span data-stu-id="d99c0-112">'T</span></span>



## <a name="remarks"></a><span data-ttu-id="d99c0-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d99c0-113">Remarks</span></span>

<span data-ttu-id="d99c0-114">Diese Funktion soll von Simulationslauf Zeiten emuliert werden, um Weiterleitungs formatierte Widersprüche zuzulassen.</span><span class="sxs-lookup"><span data-stu-id="d99c0-114">This function is intended to be emulated by simulation runtimes, so as to allow forwarding formatted contradictions.</span></span>