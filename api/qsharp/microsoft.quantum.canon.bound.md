---
uid: Microsoft.Quantum.Canon.Bound
title: Gebundene Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Bound
qsharp.summary: Given an array of operations acting on a single input, produces a new operation that performs each given operation in sequence.
ms.openlocfilehash: c12ce37054ddde1b98778888e90916c6e4725814
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96207597"
---
# <a name="bound-function"></a><span data-ttu-id="51c7c-102">Gebundene Funktion</span><span class="sxs-lookup"><span data-stu-id="51c7c-102">Bound function</span></span>

<span data-ttu-id="51c7c-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="51c7c-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="51c7c-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="51c7c-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="51c7c-105">Bei einem Array von Vorgängen, die für eine einzelne Eingabe agieren, erzeugt einen neuen Vorgang, der jeden gegebenen Vorgang nacheinander ausführt.</span><span class="sxs-lookup"><span data-stu-id="51c7c-105">Given an array of operations acting on a single input, produces a new operation that performs each given operation in sequence.</span></span>

```qsharp
function Bound<'T> (operations : ('T => Unit)[]) : ('T => Unit)
```


## <a name="input"></a><span data-ttu-id="51c7c-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="51c7c-106">Input</span></span>

### <a name="operations--t--unit-"></a><span data-ttu-id="51c7c-107">Vorgänge: 't => [Unit](xref:microsoft.quantum.lang-ref.unit) []</span><span class="sxs-lookup"><span data-stu-id="51c7c-107">operations : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) []</span></span>

<span data-ttu-id="51c7c-108">Eine Sequenz von Vorgängen, die für eine angegebene Eingabe ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="51c7c-108">A sequence of operations to be performed on a given input.</span></span>



## <a name="output--t--unit"></a><span data-ttu-id="51c7c-109">Ausgabe: 't => [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="51c7c-109">Output : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="51c7c-110">Ein neuer Vorgang, der jeden gegebenen Vorgang nacheinander für seine Eingabe ausführt.</span><span class="sxs-lookup"><span data-stu-id="51c7c-110">A new operation that performs each given operation in sequence on its input.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="51c7c-111">Typparameter</span><span class="sxs-lookup"><span data-stu-id="51c7c-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="51c7c-112">GIF</span><span class="sxs-lookup"><span data-stu-id="51c7c-112">'T</span></span>

<span data-ttu-id="51c7c-113">Das Ziel, auf dem die einzelnen Vorgänge im Array agieren.</span><span class="sxs-lookup"><span data-stu-id="51c7c-113">The target on which each of the operations in the array act.</span></span>

## <a name="see-also"></a><span data-ttu-id="51c7c-114">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="51c7c-114">See Also</span></span>

- [<span data-ttu-id="51c7c-115">Microsoft. Quantum. Canon. boundc</span><span class="sxs-lookup"><span data-stu-id="51c7c-115">Microsoft.Quantum.Canon.BoundC</span></span>](xref:Microsoft.Quantum.Canon.BoundC)
- [<span data-ttu-id="51c7c-116">Microsoft. Quantum. Canon. bounda</span><span class="sxs-lookup"><span data-stu-id="51c7c-116">Microsoft.Quantum.Canon.BoundA</span></span>](xref:Microsoft.Quantum.Canon.BoundA)
- [<span data-ttu-id="51c7c-117">Microsoft. Quantum. Canon. boundca</span><span class="sxs-lookup"><span data-stu-id="51c7c-117">Microsoft.Quantum.Canon.BoundCA</span></span>](xref:Microsoft.Quantum.Canon.BoundCA)