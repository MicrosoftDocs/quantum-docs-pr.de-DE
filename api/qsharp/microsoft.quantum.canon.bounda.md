---
uid: Microsoft.Quantum.Canon.BoundA
title: Bounda-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: BoundA
qsharp.summary: Given an array of operations acting on a single input, produces a new operation that performs each given operation in sequence. The modifier `A` indicates that all operations in the array are adjointable.
ms.openlocfilehash: 3132bf198e98dd1a2b433f36b000060e7e721865
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96216947"
---
# <a name="bounda-function"></a><span data-ttu-id="cc2e6-102">Bounda-Funktion</span><span class="sxs-lookup"><span data-stu-id="cc2e6-102">BoundA function</span></span>

<span data-ttu-id="cc2e6-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="cc2e6-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="cc2e6-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="cc2e6-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="cc2e6-105">Bei einem Array von Vorgängen, die für eine einzelne Eingabe agieren, erzeugt einen neuen Vorgang, der jeden gegebenen Vorgang nacheinander ausführt.</span><span class="sxs-lookup"><span data-stu-id="cc2e6-105">Given an array of operations acting on a single input, produces a new operation that performs each given operation in sequence.</span></span>
<span data-ttu-id="cc2e6-106">Der-Modifizierer `A` gibt an, dass alle Vorgänge im Array adjointable sind.</span><span class="sxs-lookup"><span data-stu-id="cc2e6-106">The modifier `A` indicates that all operations in the array are adjointable.</span></span>

```qsharp
function BoundA<'T> (operations : ('T => Unit is Adj)[]) : ('T => Unit is Adj)
```


## <a name="input"></a><span data-ttu-id="cc2e6-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="cc2e6-107">Input</span></span>

### <a name="operations--t--unit--is-adj"></a><span data-ttu-id="cc2e6-108">Vorgänge: 't => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ []</span><span class="sxs-lookup"><span data-stu-id="cc2e6-108">operations : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj[]</span></span>

<span data-ttu-id="cc2e6-109">Eine Sequenz von Vorgängen, die für eine angegebene Eingabe ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="cc2e6-109">A sequence of operations to be performed on a given input.</span></span>



## <a name="output--t--unit--is-adj"></a><span data-ttu-id="cc2e6-110">Ausgabe: 't => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ</span><span class="sxs-lookup"><span data-stu-id="cc2e6-110">Output : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="cc2e6-111">Ein neuer Vorgang, der jeden gegebenen Vorgang nacheinander für seine Eingabe ausführt.</span><span class="sxs-lookup"><span data-stu-id="cc2e6-111">A new operation that performs each given operation in sequence on its input.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="cc2e6-112">Typparameter</span><span class="sxs-lookup"><span data-stu-id="cc2e6-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="cc2e6-113">GIF</span><span class="sxs-lookup"><span data-stu-id="cc2e6-113">'T</span></span>

<span data-ttu-id="cc2e6-114">Das Ziel, auf dem die einzelnen Vorgänge im Array agieren.</span><span class="sxs-lookup"><span data-stu-id="cc2e6-114">The target on which each of the operations in the array act.</span></span>

## <a name="see-also"></a><span data-ttu-id="cc2e6-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="cc2e6-115">See Also</span></span>

- [<span data-ttu-id="cc2e6-116">Microsoft. Quantum. Canon. Bound</span><span class="sxs-lookup"><span data-stu-id="cc2e6-116">Microsoft.Quantum.Canon.Bound</span></span>](xref:Microsoft.Quantum.Canon.Bound)