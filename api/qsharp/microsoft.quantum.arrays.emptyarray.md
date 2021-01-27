---
uid: Microsoft.Quantum.Arrays.EmptyArray
title: Emptyarray-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: EmptyArray
qsharp.summary: Returns the empty array of a given type.
ms.openlocfilehash: cf15e61862bb64fb3408db2318fafb56d532b365
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846174"
---
# <a name="emptyarray-function"></a><span data-ttu-id="f2d13-102">Emptyarray-Funktion</span><span class="sxs-lookup"><span data-stu-id="f2d13-102">EmptyArray function</span></span>

<span data-ttu-id="f2d13-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="f2d13-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="f2d13-104">Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="f2d13-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="f2d13-105">Gibt das leere Array eines angegebenen Typs zurück.</span><span class="sxs-lookup"><span data-stu-id="f2d13-105">Returns the empty array of a given type.</span></span>

```qsharp
function EmptyArray<'TElement> () : 'TElement[]
```


## <a name="output--telement"></a><span data-ttu-id="f2d13-106">Ausgabe: ' telements []</span><span class="sxs-lookup"><span data-stu-id="f2d13-106">Output : 'TElement[]</span></span>

<span data-ttu-id="f2d13-107">Das leere Array.</span><span class="sxs-lookup"><span data-stu-id="f2d13-107">The empty array.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="f2d13-108">Typparameter</span><span class="sxs-lookup"><span data-stu-id="f2d13-108">Type Parameters</span></span>

### <a name="telement"></a><span data-ttu-id="f2d13-109">' Telements '</span><span class="sxs-lookup"><span data-stu-id="f2d13-109">'TElement</span></span>

<span data-ttu-id="f2d13-110">Der Typ der Elemente des Arrays.</span><span class="sxs-lookup"><span data-stu-id="f2d13-110">The type of elements of the array.</span></span>

## <a name="example"></a><span data-ttu-id="f2d13-111">Beispiel</span><span class="sxs-lookup"><span data-stu-id="f2d13-111">Example</span></span>

```qsharp
let empty = EmptyArray<Int>();
```