---
uid: Microsoft.Quantum.Diagnostics.AllEqualityFactB
title: Allequalityfaktb-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AllEqualityFactB
qsharp.summary: Asserts that two arrays of boolean values are equal.
ms.openlocfilehash: 725291e8b5d12683ad580d5938dadd561831e88e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853555"
---
# <a name="allequalityfactb-function"></a><span data-ttu-id="579a4-102">Allequalityfaktb-Funktion</span><span class="sxs-lookup"><span data-stu-id="579a4-102">AllEqualityFactB function</span></span>

<span data-ttu-id="579a4-103">Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="579a4-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="579a4-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="579a4-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="579a4-105">Bestätigt, dass zwei Arrays von booleschen Werten gleich sind.</span><span class="sxs-lookup"><span data-stu-id="579a4-105">Asserts that two arrays of boolean values are equal.</span></span>

```qsharp
function AllEqualityFactB (actual : Bool[], expected : Bool[], message : String) : Unit
```


## <a name="input"></a><span data-ttu-id="579a4-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="579a4-106">Input</span></span>

### <a name="actual--bool"></a><span data-ttu-id="579a4-107">tatsächlicher Wert: [bool](xref:microsoft.quantum.lang-ref.bool)[]</span><span class="sxs-lookup"><span data-stu-id="579a4-107">actual : [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span></span>

<span data-ttu-id="579a4-108">Das Array, das von einem interessanten Testfall erzeugt wird.</span><span class="sxs-lookup"><span data-stu-id="579a4-108">The array that is produced by a test case of interest.</span></span>


### <a name="expected--bool"></a><span data-ttu-id="579a4-109">erwartet: [bool](xref:microsoft.quantum.lang-ref.bool)[]</span><span class="sxs-lookup"><span data-stu-id="579a4-109">expected : [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span></span>

<span data-ttu-id="579a4-110">Das Array, das von einem interessanten Testfall erwartet wird.</span><span class="sxs-lookup"><span data-stu-id="579a4-110">The array that is expected from a test case of interest.</span></span>


### <a name="message--string"></a><span data-ttu-id="579a4-111">Message: [Zeichenfolge](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="579a4-111">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="579a4-112">Eine Meldung, die gedruckt werden soll, wenn die Arrays nicht gleich sind.</span><span class="sxs-lookup"><span data-stu-id="579a4-112">A message to be printed if the arrays are not equal.</span></span>



## <a name="output--unit"></a><span data-ttu-id="579a4-113">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="579a4-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

