---
uid: Microsoft.Quantum.Logical.GreaterThanD
title: Greaterthand-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: GreaterThanD
qsharp.summary: Returns true if and only if a number is greater than another number.
ms.openlocfilehash: 26a963645758b6de83654304c38830af5c561b3a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98849218"
---
# <a name="greaterthand-function"></a><span data-ttu-id="4bf86-102">Greaterthand-Funktion</span><span class="sxs-lookup"><span data-stu-id="4bf86-102">GreaterThanD function</span></span>

<span data-ttu-id="4bf86-103">Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="4bf86-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="4bf86-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="4bf86-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="4bf86-105">Gibt nur dann true zurück, wenn eine Zahl größer als eine andere Zahl ist.</span><span class="sxs-lookup"><span data-stu-id="4bf86-105">Returns true if and only if a number is greater than another number.</span></span>

```qsharp
function GreaterThanD (a : Double, b : Double) : Bool
```


## <a name="input"></a><span data-ttu-id="4bf86-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="4bf86-106">Input</span></span>

### <a name="a--double"></a><span data-ttu-id="4bf86-107">a: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="4bf86-107">a : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="4bf86-108">Der erste zu vergleichende Wert.</span><span class="sxs-lookup"><span data-stu-id="4bf86-108">The first value to be compared.</span></span>


### <a name="b--double"></a><span data-ttu-id="4bf86-109">b: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="4bf86-109">b : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="4bf86-110">Der zweite zu vergleichende Wert.</span><span class="sxs-lookup"><span data-stu-id="4bf86-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="4bf86-111">Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="4bf86-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="4bf86-112">`true` , wenn und nur, wenn `a` streng größer als ist `b` .</span><span class="sxs-lookup"><span data-stu-id="4bf86-112">`true` if and only if `a` is strictly greater than `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="4bf86-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4bf86-113">Remarks</span></span>

<span data-ttu-id="4bf86-114">Die folgenden sind gleichwertig:</span><span class="sxs-lookup"><span data-stu-id="4bf86-114">The following are equivalent:</span></span>

```qsharp
let cond = a > b;
let cond = GreaterThanD(a, b);
```