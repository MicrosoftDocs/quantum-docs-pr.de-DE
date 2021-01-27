---
uid: Microsoft.Quantum.Diagnostics.Fact
title: Fact-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: Fact
qsharp.summary: Declares that a classical condition is true.
ms.openlocfilehash: 8e86000f04c01040d420c2f682fc1b4ccf35cf39
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853322"
---
# <a name="fact-function"></a><span data-ttu-id="722fd-102">Fact-Funktion</span><span class="sxs-lookup"><span data-stu-id="722fd-102">Fact function</span></span>

<span data-ttu-id="722fd-103">Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="722fd-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="722fd-104">Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="722fd-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="722fd-105">Deklariert, dass eine klassische Bedingung true ist.</span><span class="sxs-lookup"><span data-stu-id="722fd-105">Declares that a classical condition is true.</span></span>

```qsharp
function Fact (actual : Bool, message : String) : Unit
```


## <a name="input"></a><span data-ttu-id="722fd-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="722fd-106">Input</span></span>

### <a name="actual--bool"></a><span data-ttu-id="722fd-107">tatsächlicher Wert: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="722fd-107">actual : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="722fd-108">Die zu deklarier Ende Bedingung.</span><span class="sxs-lookup"><span data-stu-id="722fd-108">The condition to be declared.</span></span>


### <a name="message--string"></a><span data-ttu-id="722fd-109">Message: [Zeichenfolge](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="722fd-109">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="722fd-110">Die Fehlermeldungs Zeichenfolge, die gedruckt werden soll, wenn die klassische Bedingung false ist.</span><span class="sxs-lookup"><span data-stu-id="722fd-110">Failure message string to be printed in the case that the classical condition is false.</span></span>



## <a name="output--unit"></a><span data-ttu-id="722fd-111">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="722fd-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="example"></a><span data-ttu-id="722fd-112">Beispiel</span><span class="sxs-lookup"><span data-stu-id="722fd-112">Example</span></span>

<span data-ttu-id="722fd-113">Der folgende f #-Code Ausschnitt schlägt fehl:</span><span class="sxs-lookup"><span data-stu-id="722fd-113">The following Q# snippet will fail:</span></span>

```qsharp
Fact(false, "Expected true.");
```

## <a name="see-also"></a><span data-ttu-id="722fd-114">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="722fd-114">See Also</span></span>

- [<span data-ttu-id="722fd-115">Microsoft. Quantum. Diagnostics. Widersprüchlichkeit</span><span class="sxs-lookup"><span data-stu-id="722fd-115">Microsoft.Quantum.Diagnostics.Contradiction</span></span>](xref:Microsoft.Quantum.Diagnostics.Contradiction)