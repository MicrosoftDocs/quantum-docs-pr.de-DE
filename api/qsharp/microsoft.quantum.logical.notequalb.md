---
uid: Microsoft.Quantum.Logical.NotEqualB
title: Notequalb-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: NotEqualB
qsharp.summary: Returns true if and only if two inputs are not equal.
ms.openlocfilehash: 9f362b9e08f8a798bf7f7d9c323fee6576dccd9f
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98814420"
---
# <a name="notequalb-function"></a><span data-ttu-id="66b14-102">Notequalb-Funktion</span><span class="sxs-lookup"><span data-stu-id="66b14-102">NotEqualB function</span></span>

<span data-ttu-id="66b14-103">Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="66b14-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="66b14-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="66b14-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="66b14-105">Gibt nur dann true zurück, wenn zwei Eingaben nicht gleich sind.</span><span class="sxs-lookup"><span data-stu-id="66b14-105">Returns true if and only if two inputs are not equal.</span></span>

```qsharp
function NotEqualB (a : Bool, b : Bool) : Bool
```


## <a name="input"></a><span data-ttu-id="66b14-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="66b14-106">Input</span></span>

### <a name="a--bool"></a><span data-ttu-id="66b14-107">a: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="66b14-107">a : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="66b14-108">Der erste zu vergleichende Wert.</span><span class="sxs-lookup"><span data-stu-id="66b14-108">The first value to be compared.</span></span>


### <a name="b--bool"></a><span data-ttu-id="66b14-109">b: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="66b14-109">b : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="66b14-110">Der zweite zu vergleichende Wert.</span><span class="sxs-lookup"><span data-stu-id="66b14-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="66b14-111">Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="66b14-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="66b14-112">`true``a`, wenn nicht gleich ist `b` .</span><span class="sxs-lookup"><span data-stu-id="66b14-112">`true` if and only if `a` is not equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="66b14-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="66b14-113">Remarks</span></span>

<span data-ttu-id="66b14-114">Die folgenden sind gleichwertig:</span><span class="sxs-lookup"><span data-stu-id="66b14-114">The following are equivalent:</span></span>

```qsharp
let cond = a != b;
let cond = NotEqualB(a, b);
```