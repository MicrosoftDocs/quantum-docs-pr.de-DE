---
uid: Microsoft.Quantum.Synthesis.RMEncoding
title: Rmencoding-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: RMEncoding
qsharp.summary: '{-1,1} coding of a Boolean truth value'
ms.openlocfilehash: f3c54d2e40511dacb21618b4eaf1eef9f4903f9f
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855344"
---
# <a name="rmencoding-function"></a><span data-ttu-id="ca252-102">Rmencoding-Funktion</span><span class="sxs-lookup"><span data-stu-id="ca252-102">RMEncoding function</span></span>

<span data-ttu-id="ca252-103">Namespace: [Microsoft. Quantum. Synthese](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="ca252-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="ca252-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="ca252-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="ca252-105">{-1,1} Codieren eines booleschen Wahrheits Werts</span><span class="sxs-lookup"><span data-stu-id="ca252-105">{-1,1} coding of a Boolean truth value</span></span>

```qsharp
function RMEncoding (b : Bool) : Int
```


## <a name="input"></a><span data-ttu-id="ca252-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ca252-106">Input</span></span>

### <a name="b--bool"></a><span data-ttu-id="ca252-107">b: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="ca252-107">b : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="ca252-108">Boolescher Wert</span><span class="sxs-lookup"><span data-stu-id="ca252-108">Boolean value</span></span>



## <a name="output--int"></a><span data-ttu-id="ca252-109">Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="ca252-109">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="ca252-110">1, wenn `b` false ist, andernfalls-1.</span><span class="sxs-lookup"><span data-stu-id="ca252-110">1, if `b` is false, otherwise -1</span></span>