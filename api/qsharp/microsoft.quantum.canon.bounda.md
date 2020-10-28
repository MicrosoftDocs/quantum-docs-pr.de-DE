---
uid: Microsoft.Quantum.Canon.BoundA
title: Bounda-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: BoundA
qsharp.summary: Given an array of operations acting on a single input, produces a new operation that performs each given operation in sequence. The modifier `A` indicates that all operations in the array are adjointable.
ms.openlocfilehash: 40c112d0572dc4eebfc284c9ef29f43706e20c64
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704466"
---
# <a name="bounda-function"></a><span data-ttu-id="08f85-102">Bounda-Funktion</span><span class="sxs-lookup"><span data-stu-id="08f85-102">BoundA function</span></span>

<span data-ttu-id="08f85-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="08f85-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="08f85-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="08f85-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="08f85-105">Bei einem Array von Vorgängen, die für eine einzelne Eingabe agieren, erzeugt einen neuen Vorgang, der jeden gegebenen Vorgang nacheinander ausführt.</span><span class="sxs-lookup"><span data-stu-id="08f85-105">Given an array of operations acting on a single input, produces a new operation that performs each given operation in sequence.</span></span>
<span data-ttu-id="08f85-106">Der-Modifizierer `A` gibt an, dass alle Vorgänge im Array adjointable sind.</span><span class="sxs-lookup"><span data-stu-id="08f85-106">The modifier `A` indicates that all operations in the array are adjointable.</span></span>

```qsharp
function BoundA<'T> (operations : ('T => Unit is Adj)[]) : ('T => Unit is Adj)
```


## <a name="input"></a><span data-ttu-id="08f85-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="08f85-107">Input</span></span>

### <a name="operations--t--unit-adj"></a><span data-ttu-id="08f85-108">Vorgänge: 't => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ []</span><span class="sxs-lookup"><span data-stu-id="08f85-108">operations : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj[]</span></span>

<span data-ttu-id="08f85-109">Eine Sequenz von Vorgängen, die für eine angegebene Eingabe ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="08f85-109">A sequence of operations to be performed on a given input.</span></span>



## <a name="output--t--unit-adj"></a><span data-ttu-id="08f85-110">Ausgabe: 't => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ</span><span class="sxs-lookup"><span data-stu-id="08f85-110">Output : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="08f85-111">Ein neuer Vorgang, der jeden gegebenen Vorgang nacheinander für seine Eingabe ausführt.</span><span class="sxs-lookup"><span data-stu-id="08f85-111">A new operation that performs each given operation in sequence on its input.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="08f85-112">Typparameter</span><span class="sxs-lookup"><span data-stu-id="08f85-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="08f85-113">GIF</span><span class="sxs-lookup"><span data-stu-id="08f85-113">'T</span></span>

<span data-ttu-id="08f85-114">Das Ziel, auf dem die einzelnen Vorgänge im Array agieren.</span><span class="sxs-lookup"><span data-stu-id="08f85-114">The target on which each of the operations in the array act.</span></span>

## <a name="see-also"></a><span data-ttu-id="08f85-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="08f85-115">See Also</span></span>

- [<span data-ttu-id="08f85-116">Microsoft. Quantum. Canon. Bound</span><span class="sxs-lookup"><span data-stu-id="08f85-116">Microsoft.Quantum.Canon.Bound</span></span>](xref:Microsoft.Quantum.Canon.Bound)