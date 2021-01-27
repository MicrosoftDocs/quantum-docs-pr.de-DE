---
uid: Microsoft.Quantum.Logical.LessThanLexographic
title: Lessthanlexgraphiofunktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: LessThanLexographic
qsharp.summary: Used to implement `LexographicComparison`.
ms.openlocfilehash: 716f58b747e9f58c338670271bb2e7aed96fe98c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98815643"
---
# <a name="lessthanlexographic-function"></a><span data-ttu-id="8d778-102">Lessthanlexgraphiofunktion</span><span class="sxs-lookup"><span data-stu-id="8d778-102">LessThanLexographic function</span></span>

<span data-ttu-id="8d778-103">Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="8d778-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="8d778-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="8d778-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="8d778-105">Wird verwendet, um zu implementieren `LexographicComparison` .</span><span class="sxs-lookup"><span data-stu-id="8d778-105">Used to implement `LexographicComparison`.</span></span>

```qsharp
function LessThanLexographic<'T> (comparison : (('T, 'T) -> Bool), left : 'T[], right : 'T[]) : Bool
```


## <a name="input"></a><span data-ttu-id="8d778-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8d778-106">Input</span></span>

### <a name="comparison--tt---bool"></a><span data-ttu-id="8d778-107">Vergleich: ('t, 't)-> [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="8d778-107">comparison : ('T,'T) -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>




### <a name="left--t"></a><span data-ttu-id="8d778-108">Left: 't []</span><span class="sxs-lookup"><span data-stu-id="8d778-108">left : 'T[]</span></span>




### <a name="right--t"></a><span data-ttu-id="8d778-109">Right: 't []</span><span class="sxs-lookup"><span data-stu-id="8d778-109">right : 'T[]</span></span>





## <a name="output--bool"></a><span data-ttu-id="8d778-110">Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="8d778-110">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="8d778-111">Typparameter</span><span class="sxs-lookup"><span data-stu-id="8d778-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="8d778-112">GIF</span><span class="sxs-lookup"><span data-stu-id="8d778-112">'T</span></span>

