---
uid: Microsoft.Quantum.Arrays.Reversed
title: Umgekehrte Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Reversed
qsharp.summary: Create an array that contains the same elements as an input array but in Reversed order.
ms.openlocfilehash: 50699465711de45ff994095e6c098550d637d608
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845458"
---
# <a name="reversed-function"></a><span data-ttu-id="25de6-102">Umgekehrte Funktion</span><span class="sxs-lookup"><span data-stu-id="25de6-102">Reversed function</span></span>

<span data-ttu-id="25de6-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="25de6-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="25de6-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="25de6-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="25de6-105">Erstellen Sie ein Array, das dieselben Elemente wie ein Eingabe Array, jedoch in umgekehrter Reihenfolge enthält.</span><span class="sxs-lookup"><span data-stu-id="25de6-105">Create an array that contains the same elements as an input array but in Reversed order.</span></span>

```qsharp
function Reversed<'T> (array : 'T[]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="25de6-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="25de6-106">Input</span></span>

### <a name="array--t"></a><span data-ttu-id="25de6-107">Array: 't []</span><span class="sxs-lookup"><span data-stu-id="25de6-107">array : 'T[]</span></span>

<span data-ttu-id="25de6-108">Ein Array, dessen Elemente in umgekehrter Reihenfolge kopiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="25de6-108">An array whose elements are to be copied in Reversed order.</span></span>



## <a name="output--t"></a><span data-ttu-id="25de6-109">Ausgabe: 't []</span><span class="sxs-lookup"><span data-stu-id="25de6-109">Output : 'T[]</span></span>

<span data-ttu-id="25de6-110">Ein Array, das die Elemente enthält `array[Length(array) - 1]` .</span><span class="sxs-lookup"><span data-stu-id="25de6-110">An array containing the elements `array[Length(array) - 1]` ..</span></span> <span data-ttu-id="25de6-111">`array[0]`.</span><span class="sxs-lookup"><span data-stu-id="25de6-111">`array[0]`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="25de6-112">Typparameter</span><span class="sxs-lookup"><span data-stu-id="25de6-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="25de6-113">GIF</span><span class="sxs-lookup"><span data-stu-id="25de6-113">'T</span></span>

<span data-ttu-id="25de6-114">Der Typ der Arrayelemente.</span><span class="sxs-lookup"><span data-stu-id="25de6-114">The type of the array elements.</span></span>