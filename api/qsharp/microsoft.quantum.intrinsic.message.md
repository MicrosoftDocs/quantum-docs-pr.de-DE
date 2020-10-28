---
uid: Microsoft.Quantum.Intrinsic.Message
title: Message-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: Message
qsharp.summary: Logs a message.
ms.openlocfilehash: 0428a46bc639bc8a0697f5bd392f85b8b9f40ee5
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702090"
---
# <a name="message-function"></a><span data-ttu-id="a7912-102">Message-Funktion</span><span class="sxs-lookup"><span data-stu-id="a7912-102">Message function</span></span>

<span data-ttu-id="a7912-103">Namespace: [Microsoft. Quantum. intrinsisch](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="a7912-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="a7912-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="a7912-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="a7912-105">Protokolliert eine Meldung.</span><span class="sxs-lookup"><span data-stu-id="a7912-105">Logs a message.</span></span>

```qsharp
function Message (msg : String) : Unit
```


## <a name="input"></a><span data-ttu-id="a7912-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a7912-106">Input</span></span>

### <a name="msg--string"></a><span data-ttu-id="a7912-107">msg: [Zeichenfolge](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="a7912-107">msg : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="a7912-108">Die Meldung, die gemeldet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a7912-108">The message to be reported.</span></span>



## <a name="output--unit"></a><span data-ttu-id="a7912-109">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="a7912-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="a7912-110">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a7912-110">Remarks</span></span>

<span data-ttu-id="a7912-111">Das spezifische Verhalten dieser Funktion ist simulatorabhängig, aber in den meisten Fällen wird die angegebene Nachricht in die Konsole geschrieben.</span><span class="sxs-lookup"><span data-stu-id="a7912-111">The specific behavior of this function is simulator-dependent, but in most cases the given message will be written to the console.</span></span>