---
uid: Microsoft.Quantum.Logical.Not
title: Not-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: Not
qsharp.summary: Returns the Boolean negation of a value.
ms.openlocfilehash: 3a688aac0178a2f4127496c1009fe7d5ee7ae198
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92701423"
---
# <a name="not-function"></a><span data-ttu-id="762bd-102">Not-Funktion</span><span class="sxs-lookup"><span data-stu-id="762bd-102">Not function</span></span>

<span data-ttu-id="762bd-103">Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="762bd-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="762bd-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="762bd-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="762bd-105">Gibt die boolesche Negation eines Werts zurück.</span><span class="sxs-lookup"><span data-stu-id="762bd-105">Returns the Boolean negation of a value.</span></span>

```qsharp
function Not (value : Bool) : Bool
```


## <a name="input"></a><span data-ttu-id="762bd-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="762bd-106">Input</span></span>

### <a name="value--bool"></a><span data-ttu-id="762bd-107">Wert: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="762bd-107">value : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="762bd-108">Der Wert, der negiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="762bd-108">The value to be negated.</span></span>



## <a name="output--bool"></a><span data-ttu-id="762bd-109">Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="762bd-109">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="762bd-110">`true` nur dann, wenn den Wert hat `value` `false` .</span><span class="sxs-lookup"><span data-stu-id="762bd-110">`true` if and only if `value` is `false`.</span></span>

## <a name="remarks"></a><span data-ttu-id="762bd-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="762bd-111">Remarks</span></span>

<span data-ttu-id="762bd-112">Die folgenden sind gleichwertig:</span><span class="sxs-lookup"><span data-stu-id="762bd-112">The following are equivalent:</span></span>

```Q#
let x = not value;
let x = Not(value);
```