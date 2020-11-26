---
uid: Microsoft.Quantum.Arrays.ConstantArray
title: Constantarray-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: ConstantArray
qsharp.summary: Creates an array of given length with all elements equal to given value.
ms.openlocfilehash: 8cba68af2f1e178a1ef96921283f85e4feb498ea
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96210062"
---
# <a name="constantarray-function"></a><span data-ttu-id="a0cfd-102">Constantarray-Funktion</span><span class="sxs-lookup"><span data-stu-id="a0cfd-102">ConstantArray function</span></span>

<span data-ttu-id="a0cfd-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="a0cfd-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="a0cfd-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a0cfd-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="a0cfd-105">Erstellt ein Array mit der angegebenen Länge, wobei alle Elemente gleich dem angegebenen Wert sind.</span><span class="sxs-lookup"><span data-stu-id="a0cfd-105">Creates an array of given length with all elements equal to given value.</span></span>

```qsharp
function ConstantArray<'T> (length : Int, value : 'T) : 'T[]
```


## <a name="input"></a><span data-ttu-id="a0cfd-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a0cfd-106">Input</span></span>

### <a name="length--int"></a><span data-ttu-id="a0cfd-107">Länge: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="a0cfd-107">length : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="a0cfd-108">Länge des neuen Arrays.</span><span class="sxs-lookup"><span data-stu-id="a0cfd-108">Length of the new array.</span></span>


### <a name="value--t"></a><span data-ttu-id="a0cfd-109">Wert: 't</span><span class="sxs-lookup"><span data-stu-id="a0cfd-109">value : 'T</span></span>

<span data-ttu-id="a0cfd-110">Der Wert jedes Elements des neuen Arrays.</span><span class="sxs-lookup"><span data-stu-id="a0cfd-110">The value of each element of the new array.</span></span>



## <a name="output--t"></a><span data-ttu-id="a0cfd-111">Ausgabe: 't []</span><span class="sxs-lookup"><span data-stu-id="a0cfd-111">Output : 'T[]</span></span>

<span data-ttu-id="a0cfd-112">Ein neues Array der Länge `length` , sodass jedes Element ist `value` .</span><span class="sxs-lookup"><span data-stu-id="a0cfd-112">A new array of length `length`, such that every element is `value`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="a0cfd-113">Typparameter</span><span class="sxs-lookup"><span data-stu-id="a0cfd-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="a0cfd-114">GIF</span><span class="sxs-lookup"><span data-stu-id="a0cfd-114">'T</span></span>

