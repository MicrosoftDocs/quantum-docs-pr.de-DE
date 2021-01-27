---
uid: Microsoft.Quantum.Logical.Xor
title: XOR-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: Xor
qsharp.summary: Returns the Boolean exclusive disjunction of two values.
ms.openlocfilehash: 4a4af7f628ca64170e046584d9caffe7ceee3d56
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848451"
---
# <a name="xor-function"></a><span data-ttu-id="5ebfb-102">XOR-Funktion</span><span class="sxs-lookup"><span data-stu-id="5ebfb-102">Xor function</span></span>

<span data-ttu-id="5ebfb-103">Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="5ebfb-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="5ebfb-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="5ebfb-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="5ebfb-105">Gibt die boolesche exklusive Disjunktion von zwei Werten zurück.</span><span class="sxs-lookup"><span data-stu-id="5ebfb-105">Returns the Boolean exclusive disjunction of two values.</span></span>

```qsharp
function Xor (a : Bool, b : Bool) : Bool
```


## <a name="input"></a><span data-ttu-id="5ebfb-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5ebfb-106">Input</span></span>

### <a name="a--bool"></a><span data-ttu-id="5ebfb-107">a: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="5ebfb-107">a : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="5ebfb-108">Der erste zu berücksichtigende Wert.</span><span class="sxs-lookup"><span data-stu-id="5ebfb-108">The first value to be considered.</span></span>


### <a name="b--bool"></a><span data-ttu-id="5ebfb-109">b: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="5ebfb-109">b : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="5ebfb-110">Der zweite zu berücksichtigende Wert.</span><span class="sxs-lookup"><span data-stu-id="5ebfb-110">The second value to be considered.</span></span>



## <a name="output--bool"></a><span data-ttu-id="5ebfb-111">Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="5ebfb-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="5ebfb-112">`true` nur dann, wenn genau eines von `a` und `b` ist `true` .</span><span class="sxs-lookup"><span data-stu-id="5ebfb-112">`true` if and only if exactly one of `a` and `b` is `true`.</span></span>