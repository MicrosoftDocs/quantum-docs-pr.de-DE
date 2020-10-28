---
uid: Microsoft.Quantum.Diagnostics.FormattedFailure
title: Formattedfailure-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: FormattedFailure
qsharp.summary: Internal function used to fail with meaningful error messages.
ms.openlocfilehash: 0d7fb01ddf23cd6d79f722c8f6b691afa74a8885
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702629"
---
# <a name="formattedfailure-function"></a><span data-ttu-id="4396a-102">Formattedfailure-Funktion</span><span class="sxs-lookup"><span data-stu-id="4396a-102">FormattedFailure function</span></span>

<span data-ttu-id="4396a-103">Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="4396a-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="4396a-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="4396a-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="4396a-105">Interne Funktion, die verwendet wird, um mit aussagekräftigen Fehlermeldungen fehlschlägt</span><span class="sxs-lookup"><span data-stu-id="4396a-105">Internal function used to fail with meaningful error messages.</span></span>

```qsharp
function FormattedFailure<'T> (actual : 'T, expected : 'T, message : String) : Unit
```


## <a name="input"></a><span data-ttu-id="4396a-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="4396a-106">Input</span></span>

### <a name="actual--t"></a><span data-ttu-id="4396a-107">tatsächlicher Wert: 't</span><span class="sxs-lookup"><span data-stu-id="4396a-107">actual : 'T</span></span>




### <a name="expected--t"></a><span data-ttu-id="4396a-108">erwartet: 't</span><span class="sxs-lookup"><span data-stu-id="4396a-108">expected : 'T</span></span>




### <a name="message--string"></a><span data-ttu-id="4396a-109">Message: [Zeichenfolge](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="4396a-109">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>





## <a name="output--unit"></a><span data-ttu-id="4396a-110">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="4396a-110">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="4396a-111">Typparameter</span><span class="sxs-lookup"><span data-stu-id="4396a-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="4396a-112">GIF</span><span class="sxs-lookup"><span data-stu-id="4396a-112">'T</span></span>



## <a name="remarks"></a><span data-ttu-id="4396a-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="4396a-113">Remarks</span></span>

<span data-ttu-id="4396a-114">Diese Funktion soll von Simulationslauf Zeiten emuliert werden, um Weiterleitungs formatierte Widersprüche zuzulassen.</span><span class="sxs-lookup"><span data-stu-id="4396a-114">This function is intended to be emulated by simulation runtimes, so as to allow forwarding formatted contradictions.</span></span>