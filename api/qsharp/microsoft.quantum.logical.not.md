---
uid: Microsoft.Quantum.Logical.Not
title: Not-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: Not
qsharp.summary: Returns the Boolean negation of a value.
ms.openlocfilehash: f2db43f4a2ce83d8cad1d60aa8c481a33b0c7d44
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96197448"
---
# <a name="not-function"></a><span data-ttu-id="a6057-102">Not-Funktion</span><span class="sxs-lookup"><span data-stu-id="a6057-102">Not function</span></span>

<span data-ttu-id="a6057-103">Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="a6057-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="a6057-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a6057-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="a6057-105">Gibt die boolesche Negation eines Werts zurück.</span><span class="sxs-lookup"><span data-stu-id="a6057-105">Returns the Boolean negation of a value.</span></span>

```qsharp
function Not (value : Bool) : Bool
```


## <a name="input"></a><span data-ttu-id="a6057-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a6057-106">Input</span></span>

### <a name="value--bool"></a><span data-ttu-id="a6057-107">Wert: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="a6057-107">value : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="a6057-108">Der Wert, der negiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="a6057-108">The value to be negated.</span></span>



## <a name="output--bool"></a><span data-ttu-id="a6057-109">Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="a6057-109">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="a6057-110">`true` nur dann, wenn den Wert hat `value` `false` .</span><span class="sxs-lookup"><span data-stu-id="a6057-110">`true` if and only if `value` is `false`.</span></span>

## <a name="remarks"></a><span data-ttu-id="a6057-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a6057-111">Remarks</span></span>

<span data-ttu-id="a6057-112">Die folgenden sind gleichwertig:</span><span class="sxs-lookup"><span data-stu-id="a6057-112">The following are equivalent:</span></span>

```Q#
let x = not value;
let x = Not(value);
```