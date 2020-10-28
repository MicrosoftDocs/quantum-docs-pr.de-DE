---
uid: Microsoft.Quantum.Arrays.Reversed
title: Umgekehrte Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Reversed
qsharp.summary: Create an array that contains the same elements as an input array but in Reversed order.
ms.openlocfilehash: 99244195e581dc00db24b938f5aa1c541cd4433a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705802"
---
# <a name="reversed-function"></a><span data-ttu-id="b6857-102">Umgekehrte Funktion</span><span class="sxs-lookup"><span data-stu-id="b6857-102">Reversed function</span></span>

<span data-ttu-id="b6857-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="b6857-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="b6857-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="b6857-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="b6857-105">Erstellen Sie ein Array, das dieselben Elemente wie ein Eingabe Array, jedoch in umgekehrter Reihenfolge enthält.</span><span class="sxs-lookup"><span data-stu-id="b6857-105">Create an array that contains the same elements as an input array but in Reversed order.</span></span>

```qsharp
function Reversed<'T> (array : 'T[]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="b6857-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b6857-106">Input</span></span>

### <a name="array--t"></a><span data-ttu-id="b6857-107">Array: 't []</span><span class="sxs-lookup"><span data-stu-id="b6857-107">array : 'T[]</span></span>

<span data-ttu-id="b6857-108">Ein Array, dessen Elemente in umgekehrter Reihenfolge kopiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b6857-108">An array whose elements are to be copied in Reversed order.</span></span>



## <a name="output--t"></a><span data-ttu-id="b6857-109">Ausgabe: 't []</span><span class="sxs-lookup"><span data-stu-id="b6857-109">Output : 'T[]</span></span>

<span data-ttu-id="b6857-110">Ein Array, das die Elemente enthält `array[Length(array) - 1]` .</span><span class="sxs-lookup"><span data-stu-id="b6857-110">An array containing the elements `array[Length(array) - 1]` ..</span></span> <span data-ttu-id="b6857-111">`array[0]`.</span><span class="sxs-lookup"><span data-stu-id="b6857-111">`array[0]`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="b6857-112">Typparameter</span><span class="sxs-lookup"><span data-stu-id="b6857-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="b6857-113">GIF</span><span class="sxs-lookup"><span data-stu-id="b6857-113">'T</span></span>

<span data-ttu-id="b6857-114">Der Typ der Arrayelemente.</span><span class="sxs-lookup"><span data-stu-id="b6857-114">The type of the array elements.</span></span>