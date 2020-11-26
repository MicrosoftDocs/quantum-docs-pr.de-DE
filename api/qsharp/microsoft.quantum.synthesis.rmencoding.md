---
uid: Microsoft.Quantum.Synthesis.RMEncoding
title: Rmencoding-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: RMEncoding
qsharp.summary: '{-1,1} coding of a Boolean truth value'
ms.openlocfilehash: a506ccb637b331a392ea75383c8bd605114af059
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96202939"
---
# <a name="rmencoding-function"></a><span data-ttu-id="4f63f-102">Rmencoding-Funktion</span><span class="sxs-lookup"><span data-stu-id="4f63f-102">RMEncoding function</span></span>

<span data-ttu-id="4f63f-103">Namespace: [Microsoft. Quantum. Synthese](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="4f63f-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="4f63f-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="4f63f-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="4f63f-105">{-1,1} Codieren eines booleschen Wahrheits Werts</span><span class="sxs-lookup"><span data-stu-id="4f63f-105">{-1,1} coding of a Boolean truth value</span></span>

```qsharp
function RMEncoding (b : Bool) : Int
```


## <a name="input"></a><span data-ttu-id="4f63f-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="4f63f-106">Input</span></span>

### <a name="b--bool"></a><span data-ttu-id="4f63f-107">b: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="4f63f-107">b : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="4f63f-108">Boolescher Wert</span><span class="sxs-lookup"><span data-stu-id="4f63f-108">Boolean value</span></span>



## <a name="output--int"></a><span data-ttu-id="4f63f-109">Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="4f63f-109">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="4f63f-110">1, wenn `b` false ist, andernfalls-1.</span><span class="sxs-lookup"><span data-stu-id="4f63f-110">1, if `b` is false, otherwise -1</span></span>