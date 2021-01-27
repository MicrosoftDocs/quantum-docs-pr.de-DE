---
uid: Microsoft.Quantum.Arrays.ConstantArray
title: Constantarray-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: ConstantArray
qsharp.summary: Creates an array of given length with all elements equal to given value.
ms.openlocfilehash: a3ad8a18856888a0ca6f9dd691242156b0c044d8
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846221"
---
# <a name="constantarray-function"></a><span data-ttu-id="e5bc8-102">Constantarray-Funktion</span><span class="sxs-lookup"><span data-stu-id="e5bc8-102">ConstantArray function</span></span>

<span data-ttu-id="e5bc8-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="e5bc8-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="e5bc8-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="e5bc8-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="e5bc8-105">Erstellt ein Array mit der angegebenen Länge, wobei alle Elemente gleich dem angegebenen Wert sind.</span><span class="sxs-lookup"><span data-stu-id="e5bc8-105">Creates an array of given length with all elements equal to given value.</span></span>

```qsharp
function ConstantArray<'T> (length : Int, value : 'T) : 'T[]
```


## <a name="input"></a><span data-ttu-id="e5bc8-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e5bc8-106">Input</span></span>

### <a name="length--int"></a><span data-ttu-id="e5bc8-107">Länge: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="e5bc8-107">length : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="e5bc8-108">Länge des neuen Arrays.</span><span class="sxs-lookup"><span data-stu-id="e5bc8-108">Length of the new array.</span></span>


### <a name="value--t"></a><span data-ttu-id="e5bc8-109">Wert: 't</span><span class="sxs-lookup"><span data-stu-id="e5bc8-109">value : 'T</span></span>

<span data-ttu-id="e5bc8-110">Der Wert jedes Elements des neuen Arrays.</span><span class="sxs-lookup"><span data-stu-id="e5bc8-110">The value of each element of the new array.</span></span>



## <a name="output--t"></a><span data-ttu-id="e5bc8-111">Ausgabe: 't []</span><span class="sxs-lookup"><span data-stu-id="e5bc8-111">Output : 'T[]</span></span>

<span data-ttu-id="e5bc8-112">Ein neues Array der Länge `length` , sodass jedes Element ist `value` .</span><span class="sxs-lookup"><span data-stu-id="e5bc8-112">A new array of length `length`, such that every element is `value`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="e5bc8-113">Typparameter</span><span class="sxs-lookup"><span data-stu-id="e5bc8-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="e5bc8-114">GIF</span><span class="sxs-lookup"><span data-stu-id="e5bc8-114">'T</span></span>



## <a name="example"></a><span data-ttu-id="e5bc8-115">Beispiel</span><span class="sxs-lookup"><span data-stu-id="e5bc8-115">Example</span></span>

<span data-ttu-id="e5bc8-116">Der folgende Code erstellt ein Array von 3 booleschen Werten, die jeweils gleich sind `true` :</span><span class="sxs-lookup"><span data-stu-id="e5bc8-116">The following code creates an array of 3 Boolean values, each equal to `true`:</span></span>

```qsharp
let array = ConstantArray(3, true);
```