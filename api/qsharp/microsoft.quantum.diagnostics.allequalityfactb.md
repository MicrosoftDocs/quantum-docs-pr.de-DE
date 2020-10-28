---
uid: Microsoft.Quantum.Diagnostics.AllEqualityFactB
title: Allequalityfaktb-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AllEqualityFactB
qsharp.summary: Asserts that two arrays of boolean values are equal.
ms.openlocfilehash: 100aacccbfd5b45ac9f859cd89424b0ed4007f72
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702798"
---
# <a name="allequalityfactb-function"></a><span data-ttu-id="30582-102">Allequalityfaktb-Funktion</span><span class="sxs-lookup"><span data-stu-id="30582-102">AllEqualityFactB function</span></span>

<span data-ttu-id="30582-103">Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="30582-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="30582-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="30582-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="30582-105">Bestätigt, dass zwei Arrays von booleschen Werten gleich sind.</span><span class="sxs-lookup"><span data-stu-id="30582-105">Asserts that two arrays of boolean values are equal.</span></span>

```qsharp
function AllEqualityFactB (actual : Bool[], expected : Bool[], message : String) : Unit
```


## <a name="input"></a><span data-ttu-id="30582-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="30582-106">Input</span></span>

### <a name="actual--bool"></a><span data-ttu-id="30582-107">tatsächlicher Wert: [bool](xref:microsoft.quantum.lang-ref.bool)[]</span><span class="sxs-lookup"><span data-stu-id="30582-107">actual : [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span></span>

<span data-ttu-id="30582-108">Das Array, das von einem interessanten Testfall erzeugt wird.</span><span class="sxs-lookup"><span data-stu-id="30582-108">The array that is produced by a test case of interest.</span></span>


### <a name="expected--bool"></a><span data-ttu-id="30582-109">erwartet: [bool](xref:microsoft.quantum.lang-ref.bool)[]</span><span class="sxs-lookup"><span data-stu-id="30582-109">expected : [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span></span>

<span data-ttu-id="30582-110">Das Array, das von einem interessanten Testfall erwartet wird.</span><span class="sxs-lookup"><span data-stu-id="30582-110">The array that is expected from a test case of interest.</span></span>


### <a name="message--string"></a><span data-ttu-id="30582-111">Message: [Zeichenfolge](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="30582-111">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="30582-112">Eine Meldung, die gedruckt werden soll, wenn die Arrays nicht gleich sind.</span><span class="sxs-lookup"><span data-stu-id="30582-112">A message to be printed if the arrays are not equal.</span></span>



## <a name="output--unit"></a><span data-ttu-id="30582-113">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="30582-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

