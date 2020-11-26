---
uid: Microsoft.Quantum.Intrinsic.Message
title: Message-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: Message
qsharp.summary: Logs a message.
ms.openlocfilehash: 4eb55dd4fd8d78e4b5a9bb289dacfbdb3aa4beb8
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96199011"
---
# <a name="message-function"></a><span data-ttu-id="4356d-102">Message-Funktion</span><span class="sxs-lookup"><span data-stu-id="4356d-102">Message function</span></span>

<span data-ttu-id="4356d-103">Namespace: [Microsoft. Quantum. intrinsisch](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="4356d-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="4356d-104">Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="4356d-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="4356d-105">Protokolliert eine Meldung.</span><span class="sxs-lookup"><span data-stu-id="4356d-105">Logs a message.</span></span>

```qsharp
function Message (msg : String) : Unit
```


## <a name="input"></a><span data-ttu-id="4356d-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="4356d-106">Input</span></span>

### <a name="msg--string"></a><span data-ttu-id="4356d-107">msg: [Zeichenfolge](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="4356d-107">msg : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="4356d-108">Die Meldung, die gemeldet werden soll.</span><span class="sxs-lookup"><span data-stu-id="4356d-108">The message to be reported.</span></span>



## <a name="output--unit"></a><span data-ttu-id="4356d-109">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="4356d-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="4356d-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4356d-110">Remarks</span></span>

<span data-ttu-id="4356d-111">Das spezifische Verhalten dieser Funktion ist simulatorabhängig, aber in den meisten Fällen wird die angegebene Nachricht in die Konsole geschrieben.</span><span class="sxs-lookup"><span data-stu-id="4356d-111">The specific behavior of this function is simulator-dependent, but in most cases the given message will be written to the console.</span></span>