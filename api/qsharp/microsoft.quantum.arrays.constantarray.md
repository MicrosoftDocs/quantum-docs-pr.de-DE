---
uid: Microsoft.Quantum.Arrays.ConstantArray
title: Constantarray-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: ConstantArray
qsharp.summary: Creates an array of given length with all elements equal to given value.
ms.openlocfilehash: 848f18944829d08a10ec602dcb5d99c100c81f76
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706138"
---
# <a name="constantarray-function"></a><span data-ttu-id="28791-102">Constantarray-Funktion</span><span class="sxs-lookup"><span data-stu-id="28791-102">ConstantArray function</span></span>

<span data-ttu-id="28791-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="28791-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="28791-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="28791-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="28791-105">Erstellt ein Array mit der angegebenen Länge, wobei alle Elemente gleich dem angegebenen Wert sind.</span><span class="sxs-lookup"><span data-stu-id="28791-105">Creates an array of given length with all elements equal to given value.</span></span>

```qsharp
function ConstantArray<'T> (length : Int, value : 'T) : 'T[]
```


## <a name="input"></a><span data-ttu-id="28791-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="28791-106">Input</span></span>

### <a name="length--int"></a><span data-ttu-id="28791-107">Länge: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="28791-107">length : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="28791-108">Länge des neuen Arrays.</span><span class="sxs-lookup"><span data-stu-id="28791-108">Length of the new array.</span></span>


### <a name="value--t"></a><span data-ttu-id="28791-109">Wert: 't</span><span class="sxs-lookup"><span data-stu-id="28791-109">value : 'T</span></span>

<span data-ttu-id="28791-110">Der Wert jedes Elements des neuen Arrays.</span><span class="sxs-lookup"><span data-stu-id="28791-110">The value of each element of the new array.</span></span>



## <a name="output--t"></a><span data-ttu-id="28791-111">Ausgabe: 't []</span><span class="sxs-lookup"><span data-stu-id="28791-111">Output : 'T[]</span></span>

<span data-ttu-id="28791-112">Ein neues Array der Länge `length` , sodass jedes Element ist `value` .</span><span class="sxs-lookup"><span data-stu-id="28791-112">A new array of length `length`, such that every element is `value`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="28791-113">Typparameter</span><span class="sxs-lookup"><span data-stu-id="28791-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="28791-114">GIF</span><span class="sxs-lookup"><span data-stu-id="28791-114">'T</span></span>

