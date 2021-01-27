---
uid: Microsoft.Quantum.Logical.NotEqualD
title: Notequald-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: NotEqualD
qsharp.summary: Returns true if and only if two inputs are not equal.
ms.openlocfilehash: 38f30309a4c27a5ef7e112a09a0efe3b5512d4e3
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98849048"
---
# <a name="notequald-function"></a><span data-ttu-id="22824-102">Notequald-Funktion</span><span class="sxs-lookup"><span data-stu-id="22824-102">NotEqualD function</span></span>

<span data-ttu-id="22824-103">Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="22824-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="22824-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="22824-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="22824-105">Gibt nur dann true zurück, wenn zwei Eingaben nicht gleich sind.</span><span class="sxs-lookup"><span data-stu-id="22824-105">Returns true if and only if two inputs are not equal.</span></span>

```qsharp
function NotEqualD (a : Double, b : Double) : Bool
```


## <a name="input"></a><span data-ttu-id="22824-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="22824-106">Input</span></span>

### <a name="a--double"></a><span data-ttu-id="22824-107">a: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="22824-107">a : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="22824-108">Der erste zu vergleichende Wert.</span><span class="sxs-lookup"><span data-stu-id="22824-108">The first value to be compared.</span></span>


### <a name="b--double"></a><span data-ttu-id="22824-109">b: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="22824-109">b : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="22824-110">Der zweite zu vergleichende Wert.</span><span class="sxs-lookup"><span data-stu-id="22824-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="22824-111">Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="22824-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="22824-112">`true``a`, wenn nicht gleich ist `b` .</span><span class="sxs-lookup"><span data-stu-id="22824-112">`true` if and only if `a` is not equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="22824-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="22824-113">Remarks</span></span>

<span data-ttu-id="22824-114">Die folgenden sind gleichwertig:</span><span class="sxs-lookup"><span data-stu-id="22824-114">The following are equivalent:</span></span>

```qsharp
let cond = a != b;
let cond = NotEqualD(a, b);
```