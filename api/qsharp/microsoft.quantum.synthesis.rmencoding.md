---
uid: Microsoft.Quantum.Synthesis.RMEncoding
title: Rmencoding-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: RMEncoding
qsharp.summary: '{-1,1} coding of a Boolean truth value'
ms.openlocfilehash: ef9be0f0628c8ba8c5f131cc558bdcda6bb6ea55
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92725481"
---
# <a name="rmencoding-function"></a><span data-ttu-id="8c73f-102">Rmencoding-Funktion</span><span class="sxs-lookup"><span data-stu-id="8c73f-102">RMEncoding function</span></span>

<span data-ttu-id="8c73f-103">Namespace: [Microsoft. Quantum. Synthese](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="8c73f-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="8c73f-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="8c73f-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="8c73f-105">{-1,1} Codieren eines booleschen Wahrheits Werts</span><span class="sxs-lookup"><span data-stu-id="8c73f-105">{-1,1} coding of a Boolean truth value</span></span>

```qsharp
function RMEncoding (b : Bool) : Int
```


## <a name="input"></a><span data-ttu-id="8c73f-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8c73f-106">Input</span></span>

### <a name="b--bool"></a><span data-ttu-id="8c73f-107">b: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="8c73f-107">b : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="8c73f-108">Boolescher Wert</span><span class="sxs-lookup"><span data-stu-id="8c73f-108">Boolean value</span></span>



## <a name="output--int"></a><span data-ttu-id="8c73f-109">Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="8c73f-109">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="8c73f-110">1, wenn `b` false ist, andernfalls-1.</span><span class="sxs-lookup"><span data-stu-id="8c73f-110">1, if `b` is false, otherwise -1</span></span>