---
uid: Microsoft.Quantum.Diagnostics.Contradiction
title: Widerspruch Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: Contradiction
qsharp.summary: Declares that a classical condition is false.
ms.openlocfilehash: f9ad9a7d67bda8e50c76f679f535ad55ba07698e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96202140"
---
# <a name="contradiction-function"></a><span data-ttu-id="f0c6a-102">Widerspruch Funktion</span><span class="sxs-lookup"><span data-stu-id="f0c6a-102">Contradiction function</span></span>

<span data-ttu-id="f0c6a-103">Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="f0c6a-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="f0c6a-104">Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="f0c6a-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="f0c6a-105">Deklariert, dass eine klassische Bedingung false ist.</span><span class="sxs-lookup"><span data-stu-id="f0c6a-105">Declares that a classical condition is false.</span></span>

```qsharp
function Contradiction (actual : Bool, message : String) : Unit
```


## <a name="input"></a><span data-ttu-id="f0c6a-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f0c6a-106">Input</span></span>

### <a name="actual--bool"></a><span data-ttu-id="f0c6a-107">tatsächlicher Wert: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="f0c6a-107">actual : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="f0c6a-108">Die zu deklarier Ende Bedingung.</span><span class="sxs-lookup"><span data-stu-id="f0c6a-108">The condition to be declared.</span></span>


### <a name="message--string"></a><span data-ttu-id="f0c6a-109">Message: [Zeichenfolge](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="f0c6a-109">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="f0c6a-110">Die Fehlermeldungs Zeichenfolge, die gedruckt werden soll, wenn die klassische Bedingung "true" ist.</span><span class="sxs-lookup"><span data-stu-id="f0c6a-110">Failure message string to be printed in the case that the classical condition is true.</span></span>



## <a name="output--unit"></a><span data-ttu-id="f0c6a-111">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="f0c6a-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="f0c6a-112">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="f0c6a-112">See Also</span></span>

- [<span data-ttu-id="f0c6a-113">Microsoft. Quantum. Diagnostics. Fact</span><span class="sxs-lookup"><span data-stu-id="f0c6a-113">Microsoft.Quantum.Diagnostics.Fact</span></span>](xref:Microsoft.Quantum.Diagnostics.Fact)