---
uid: Microsoft.Quantum.Canon.BoundCA
title: Boundca-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: BoundCA
qsharp.summary: Given an array of operations acting on a single input, produces a new operation that performs each given operation in sequence. The modifier `CA` indicates that all operations in the array are adjointable and controllable.
ms.openlocfilehash: d96d33781def10940479ba2eafdcc6711a0c05a5
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704434"
---
# <a name="boundca-function"></a><span data-ttu-id="a28d6-102">Boundca-Funktion</span><span class="sxs-lookup"><span data-stu-id="a28d6-102">BoundCA function</span></span>

<span data-ttu-id="a28d6-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="a28d6-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="a28d6-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="a28d6-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="a28d6-105">Bei einem Array von Vorgängen, die für eine einzelne Eingabe agieren, erzeugt einen neuen Vorgang, der jeden gegebenen Vorgang nacheinander ausführt.</span><span class="sxs-lookup"><span data-stu-id="a28d6-105">Given an array of operations acting on a single input, produces a new operation that performs each given operation in sequence.</span></span>
<span data-ttu-id="a28d6-106">Der-Modifizierer `CA` gibt an, dass alle Vorgänge im Array adjointable und steuerbar sind.</span><span class="sxs-lookup"><span data-stu-id="a28d6-106">The modifier `CA` indicates that all operations in the array are adjointable and controllable.</span></span>

```qsharp
function BoundCA<'T> (operations : ('T => Unit is Adj + Ctl)[]) : ('T => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="a28d6-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a28d6-107">Input</span></span>

### <a name="operations--t--unit-adj--ctl"></a><span data-ttu-id="a28d6-108">Vorgänge: 't => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL []</span><span class="sxs-lookup"><span data-stu-id="a28d6-108">operations : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl[]</span></span>

<span data-ttu-id="a28d6-109">Eine Sequenz von Vorgängen, die für eine angegebene Eingabe ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a28d6-109">A sequence of operations to be performed on a given input.</span></span>



## <a name="output--t--unit-adj--ctl"></a><span data-ttu-id="a28d6-110">Ausgabe: 't => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="a28d6-110">Output : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="a28d6-111">Ein neuer Vorgang, der jeden gegebenen Vorgang nacheinander für seine Eingabe ausführt.</span><span class="sxs-lookup"><span data-stu-id="a28d6-111">A new operation that performs each given operation in sequence on its input.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="a28d6-112">Typparameter</span><span class="sxs-lookup"><span data-stu-id="a28d6-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="a28d6-113">GIF</span><span class="sxs-lookup"><span data-stu-id="a28d6-113">'T</span></span>

<span data-ttu-id="a28d6-114">Das Ziel, auf dem die einzelnen Vorgänge im Array agieren.</span><span class="sxs-lookup"><span data-stu-id="a28d6-114">The target on which each of the operations in the array act.</span></span>

## <a name="see-also"></a><span data-ttu-id="a28d6-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="a28d6-115">See Also</span></span>

- [<span data-ttu-id="a28d6-116">Microsoft. Quantum. Canon. Bound</span><span class="sxs-lookup"><span data-stu-id="a28d6-116">Microsoft.Quantum.Canon.Bound</span></span>](xref:Microsoft.Quantum.Canon.Bound)