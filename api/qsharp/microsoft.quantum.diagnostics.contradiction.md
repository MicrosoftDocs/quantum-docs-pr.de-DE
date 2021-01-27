---
uid: Microsoft.Quantum.Diagnostics.Contradiction
title: Widerspruch Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: Contradiction
qsharp.summary: Declares that a classical condition is false.
ms.openlocfilehash: 7d62c9341b768dfdfbfbf8e73e64748f04317595
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98829364"
---
# <a name="contradiction-function"></a><span data-ttu-id="9c67e-102">Widerspruch Funktion</span><span class="sxs-lookup"><span data-stu-id="9c67e-102">Contradiction function</span></span>

<span data-ttu-id="9c67e-103">Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="9c67e-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="9c67e-104">Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="9c67e-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="9c67e-105">Deklariert, dass eine klassische Bedingung false ist.</span><span class="sxs-lookup"><span data-stu-id="9c67e-105">Declares that a classical condition is false.</span></span>

```qsharp
function Contradiction (actual : Bool, message : String) : Unit
```


## <a name="input"></a><span data-ttu-id="9c67e-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="9c67e-106">Input</span></span>

### <a name="actual--bool"></a><span data-ttu-id="9c67e-107">tatsächlicher Wert: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="9c67e-107">actual : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="9c67e-108">Die zu deklarier Ende Bedingung.</span><span class="sxs-lookup"><span data-stu-id="9c67e-108">The condition to be declared.</span></span>


### <a name="message--string"></a><span data-ttu-id="9c67e-109">Message: [Zeichenfolge](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="9c67e-109">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="9c67e-110">Die Fehlermeldungs Zeichenfolge, die gedruckt werden soll, wenn die klassische Bedingung "true" ist.</span><span class="sxs-lookup"><span data-stu-id="9c67e-110">Failure message string to be printed in the case that the classical condition is true.</span></span>



## <a name="output--unit"></a><span data-ttu-id="9c67e-111">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="9c67e-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="example"></a><span data-ttu-id="9c67e-112">Beispiel</span><span class="sxs-lookup"><span data-stu-id="9c67e-112">Example</span></span>

<span data-ttu-id="9c67e-113">Der folgende f #-Code druckt "Hello, World":</span><span class="sxs-lookup"><span data-stu-id="9c67e-113">The following Q# code will print "Hello, world":</span></span>

```qsharp
Contradiction(2 == 3, "2 is not equal to 3.");
Message("Hello, world.");
```

## <a name="see-also"></a><span data-ttu-id="9c67e-114">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="9c67e-114">See Also</span></span>

- [<span data-ttu-id="9c67e-115">Microsoft. Quantum. Diagnostics. Fact</span><span class="sxs-lookup"><span data-stu-id="9c67e-115">Microsoft.Quantum.Diagnostics.Fact</span></span>](xref:Microsoft.Quantum.Diagnostics.Fact)