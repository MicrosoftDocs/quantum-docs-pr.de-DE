---
uid: Microsoft.Quantum.Diagnostics.Contradiction
title: Widerspruch Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: Contradiction
qsharp.summary: Declares that a classical condition is false.
ms.openlocfilehash: a5f3f26c5ada2eea9206699a2cc77575a9b5eebd
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702708"
---
# <a name="contradiction-function"></a><span data-ttu-id="d831a-102">Widerspruch Funktion</span><span class="sxs-lookup"><span data-stu-id="d831a-102">Contradiction function</span></span>

<span data-ttu-id="d831a-103">Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="d831a-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="d831a-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="d831a-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="d831a-105">Deklariert, dass eine klassische Bedingung false ist.</span><span class="sxs-lookup"><span data-stu-id="d831a-105">Declares that a classical condition is false.</span></span>

```qsharp
function Contradiction (actual : Bool, message : String) : Unit
```


## <a name="input"></a><span data-ttu-id="d831a-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d831a-106">Input</span></span>

### <a name="actual--bool"></a><span data-ttu-id="d831a-107">tatsächlicher Wert: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="d831a-107">actual : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="d831a-108">Die zu deklarier Ende Bedingung.</span><span class="sxs-lookup"><span data-stu-id="d831a-108">The condition to be declared.</span></span>


### <a name="message--string"></a><span data-ttu-id="d831a-109">Message: [Zeichenfolge](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="d831a-109">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="d831a-110">Die Fehlermeldungs Zeichenfolge, die gedruckt werden soll, wenn die klassische Bedingung "true" ist.</span><span class="sxs-lookup"><span data-stu-id="d831a-110">Failure message string to be printed in the case that the classical condition is true.</span></span>



## <a name="output--unit"></a><span data-ttu-id="d831a-111">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="d831a-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="d831a-112">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="d831a-112">See Also</span></span>

- [<span data-ttu-id="d831a-113">Microsoft. Quantum. Diagnostics. Fact</span><span class="sxs-lookup"><span data-stu-id="d831a-113">Microsoft.Quantum.Diagnostics.Fact</span></span>](xref:Microsoft.Quantum.Diagnostics.Fact)