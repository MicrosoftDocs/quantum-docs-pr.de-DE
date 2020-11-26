---
uid: Microsoft.Quantum.Arrays.IsEmpty
title: IsEmpty-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: IsEmpty
qsharp.summary: Returns true if and only if an array is empty.
ms.openlocfilehash: ae3ad8763987bab9fdae07a5fe9bd4aabef65205
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220976"
---
# <a name="isempty-function"></a><span data-ttu-id="32739-102">IsEmpty-Funktion</span><span class="sxs-lookup"><span data-stu-id="32739-102">IsEmpty function</span></span>

<span data-ttu-id="32739-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="32739-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="32739-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="32739-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="32739-105">Gibt nur dann true zurück, wenn ein Array leer ist.</span><span class="sxs-lookup"><span data-stu-id="32739-105">Returns true if and only if an array is empty.</span></span>

```qsharp
function IsEmpty<'T> (array : 'T[]) : Bool
```


## <a name="input"></a><span data-ttu-id="32739-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="32739-106">Input</span></span>

### <a name="array--t"></a><span data-ttu-id="32739-107">Array: 't []</span><span class="sxs-lookup"><span data-stu-id="32739-107">array : 'T[]</span></span>

<span data-ttu-id="32739-108">Das zu überprüfende Array.</span><span class="sxs-lookup"><span data-stu-id="32739-108">The array to be checked.</span></span>



## <a name="output--bool"></a><span data-ttu-id="32739-109">Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="32739-109">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="32739-110">`true` , wenn das Array leer ist (hat Länge 0).</span><span class="sxs-lookup"><span data-stu-id="32739-110">`true` if and only if the array is empty (has length 0).</span></span>

## <a name="type-parameters"></a><span data-ttu-id="32739-111">Typparameter</span><span class="sxs-lookup"><span data-stu-id="32739-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="32739-112">GIF</span><span class="sxs-lookup"><span data-stu-id="32739-112">'T</span></span>

