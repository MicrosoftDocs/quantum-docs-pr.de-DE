---
uid: Microsoft.Quantum.Logical.Not
title: Not-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: Not
qsharp.summary: Returns the Boolean negation of a value.
ms.openlocfilehash: bf09cac8d126371df6218b7e92d68a881b732dc8
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98849076"
---
# <a name="not-function"></a><span data-ttu-id="2b649-102">Not-Funktion</span><span class="sxs-lookup"><span data-stu-id="2b649-102">Not function</span></span>

<span data-ttu-id="2b649-103">Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="2b649-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="2b649-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="2b649-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="2b649-105">Gibt die boolesche Negation eines Werts zurück.</span><span class="sxs-lookup"><span data-stu-id="2b649-105">Returns the Boolean negation of a value.</span></span>

```qsharp
function Not (value : Bool) : Bool
```


## <a name="input"></a><span data-ttu-id="2b649-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2b649-106">Input</span></span>

### <a name="value--bool"></a><span data-ttu-id="2b649-107">Wert: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="2b649-107">value : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="2b649-108">Der Wert, der negiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="2b649-108">The value to be negated.</span></span>



## <a name="output--bool"></a><span data-ttu-id="2b649-109">Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="2b649-109">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="2b649-110">`true` nur dann, wenn den Wert hat `value` `false` .</span><span class="sxs-lookup"><span data-stu-id="2b649-110">`true` if and only if `value` is `false`.</span></span>

## <a name="remarks"></a><span data-ttu-id="2b649-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2b649-111">Remarks</span></span>

<span data-ttu-id="2b649-112">Die folgenden sind gleichwertig:</span><span class="sxs-lookup"><span data-stu-id="2b649-112">The following are equivalent:</span></span>

```qsharp
let x = not value;
let x = Not(value);
```