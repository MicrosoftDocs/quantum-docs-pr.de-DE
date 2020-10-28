---
uid: Microsoft.Quantum.Canon.Bound
title: Gebundene Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Bound
qsharp.summary: Given an array of operations acting on a single input, produces a new operation that performs each given operation in sequence.
ms.openlocfilehash: 34ca2b79d0ee09bd3b5b5b3f0c0b20420d5b3882
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704474"
---
# <a name="bound-function"></a><span data-ttu-id="88a60-102">Gebundene Funktion</span><span class="sxs-lookup"><span data-stu-id="88a60-102">Bound function</span></span>

<span data-ttu-id="88a60-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="88a60-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="88a60-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="88a60-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="88a60-105">Bei einem Array von Vorgängen, die für eine einzelne Eingabe agieren, erzeugt einen neuen Vorgang, der jeden gegebenen Vorgang nacheinander ausführt.</span><span class="sxs-lookup"><span data-stu-id="88a60-105">Given an array of operations acting on a single input, produces a new operation that performs each given operation in sequence.</span></span>

```qsharp
function Bound<'T> (operations : ('T => Unit)[]) : ('T => Unit)
```


## <a name="input"></a><span data-ttu-id="88a60-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="88a60-106">Input</span></span>

### <a name="operations--t--unit-"></a><span data-ttu-id="88a60-107">Vorgänge: 't => [Unit](xref:microsoft.quantum.lang-ref.unit) []</span><span class="sxs-lookup"><span data-stu-id="88a60-107">operations : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) []</span></span>

<span data-ttu-id="88a60-108">Eine Sequenz von Vorgängen, die für eine angegebene Eingabe ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="88a60-108">A sequence of operations to be performed on a given input.</span></span>



## <a name="output--t--unit"></a><span data-ttu-id="88a60-109">Ausgabe: 't => [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="88a60-109">Output : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="88a60-110">Ein neuer Vorgang, der jeden gegebenen Vorgang nacheinander für seine Eingabe ausführt.</span><span class="sxs-lookup"><span data-stu-id="88a60-110">A new operation that performs each given operation in sequence on its input.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="88a60-111">Typparameter</span><span class="sxs-lookup"><span data-stu-id="88a60-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="88a60-112">GIF</span><span class="sxs-lookup"><span data-stu-id="88a60-112">'T</span></span>

<span data-ttu-id="88a60-113">Das Ziel, auf dem die einzelnen Vorgänge im Array agieren.</span><span class="sxs-lookup"><span data-stu-id="88a60-113">The target on which each of the operations in the array act.</span></span>

## <a name="see-also"></a><span data-ttu-id="88a60-114">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="88a60-114">See Also</span></span>

- [<span data-ttu-id="88a60-115">Microsoft. Quantum. Canon. boundc</span><span class="sxs-lookup"><span data-stu-id="88a60-115">Microsoft.Quantum.Canon.BoundC</span></span>](xref:Microsoft.Quantum.Canon.BoundC)
- [<span data-ttu-id="88a60-116">Microsoft. Quantum. Canon. bounda</span><span class="sxs-lookup"><span data-stu-id="88a60-116">Microsoft.Quantum.Canon.BoundA</span></span>](xref:Microsoft.Quantum.Canon.BoundA)
- [<span data-ttu-id="88a60-117">Microsoft. Quantum. Canon. boundca</span><span class="sxs-lookup"><span data-stu-id="88a60-117">Microsoft.Quantum.Canon.BoundCA</span></span>](xref:Microsoft.Quantum.Canon.BoundCA)