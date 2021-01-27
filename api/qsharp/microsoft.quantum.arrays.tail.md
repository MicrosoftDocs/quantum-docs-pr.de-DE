---
uid: Microsoft.Quantum.Arrays.Tail
title: Tail-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Tail
qsharp.summary: Returns the last element of the array.
ms.openlocfilehash: 680562228a39263ef87ba053e6b7683412947e46
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845405"
---
# <a name="tail-function"></a><span data-ttu-id="1a4e9-102">Tail-Funktion</span><span class="sxs-lookup"><span data-stu-id="1a4e9-102">Tail function</span></span>

<span data-ttu-id="1a4e9-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="1a4e9-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="1a4e9-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="1a4e9-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="1a4e9-105">Gibt das letzte Element des Arrays zurück.</span><span class="sxs-lookup"><span data-stu-id="1a4e9-105">Returns the last element of the array.</span></span>

```qsharp
function Tail<'A> (array : 'A[]) : 'A
```


## <a name="input"></a><span data-ttu-id="1a4e9-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="1a4e9-106">Input</span></span>

### <a name="array--a"></a><span data-ttu-id="1a4e9-107">Array: ' A []</span><span class="sxs-lookup"><span data-stu-id="1a4e9-107">array : 'A[]</span></span>

<span data-ttu-id="1a4e9-108">Das Array, von dem das letzte Element entnommen wurde.</span><span class="sxs-lookup"><span data-stu-id="1a4e9-108">Array of which the last element is taken.</span></span> <span data-ttu-id="1a4e9-109">Das Array muss eine Länge von mindestens 1 aufweisen.</span><span class="sxs-lookup"><span data-stu-id="1a4e9-109">Array must have length at least 1.</span></span>



## <a name="output--a"></a><span data-ttu-id="1a4e9-110">Ausgabe: "A</span><span class="sxs-lookup"><span data-stu-id="1a4e9-110">Output : 'A</span></span>

<span data-ttu-id="1a4e9-111">Das letzte Element des Arrays.</span><span class="sxs-lookup"><span data-stu-id="1a4e9-111">The last element of the array.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="1a4e9-112">Typparameter</span><span class="sxs-lookup"><span data-stu-id="1a4e9-112">Type Parameters</span></span>

### <a name="a"></a><span data-ttu-id="1a4e9-113">"A</span><span class="sxs-lookup"><span data-stu-id="1a4e9-113">'A</span></span>

<span data-ttu-id="1a4e9-114">Der Typ der Arrayelemente.</span><span class="sxs-lookup"><span data-stu-id="1a4e9-114">The type of the array elements.</span></span>