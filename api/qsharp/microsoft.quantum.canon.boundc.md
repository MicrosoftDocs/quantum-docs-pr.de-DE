---
uid: Microsoft.Quantum.Canon.BoundC
title: Boundc-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: BoundC
qsharp.summary: Given an array of operations acting on a single input, produces a new operation that performs each given operation in sequence. The modifier `C` indicates that all operations in the array are controllable.
ms.openlocfilehash: 04dca4ff317bf3cee053f7c3903112f4e05a3973
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704455"
---
# <a name="boundc-function"></a><span data-ttu-id="32a8a-102">Boundc-Funktion</span><span class="sxs-lookup"><span data-stu-id="32a8a-102">BoundC function</span></span>

<span data-ttu-id="32a8a-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="32a8a-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="32a8a-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="32a8a-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="32a8a-105">Bei einem Array von Vorgängen, die für eine einzelne Eingabe agieren, erzeugt einen neuen Vorgang, der jeden gegebenen Vorgang nacheinander ausführt.</span><span class="sxs-lookup"><span data-stu-id="32a8a-105">Given an array of operations acting on a single input, produces a new operation that performs each given operation in sequence.</span></span>
<span data-ttu-id="32a8a-106">Der-Modifizierer `C` gibt an, dass alle Vorgänge im Array steuerbar sind.</span><span class="sxs-lookup"><span data-stu-id="32a8a-106">The modifier `C` indicates that all operations in the array are controllable.</span></span>

```qsharp
function BoundC<'T> (operations : ('T => Unit is Ctl)[]) : ('T => Unit is Ctl)
```


## <a name="input"></a><span data-ttu-id="32a8a-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="32a8a-107">Input</span></span>

### <a name="operations--t--unit-ctl"></a><span data-ttu-id="32a8a-108">Vorgänge: 't => [Unit](xref:microsoft.quantum.lang-ref.unit) CTL []</span><span class="sxs-lookup"><span data-stu-id="32a8a-108">operations : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl[]</span></span>

<span data-ttu-id="32a8a-109">Eine Sequenz von Vorgängen, die für eine angegebene Eingabe ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="32a8a-109">A sequence of operations to be performed on a given input.</span></span>



## <a name="output--t--unit-ctl"></a><span data-ttu-id="32a8a-110">Ausgabe: 't => [Unit](xref:microsoft.quantum.lang-ref.unit) CTL</span><span class="sxs-lookup"><span data-stu-id="32a8a-110">Output : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>

<span data-ttu-id="32a8a-111">Ein neuer Vorgang, der jeden gegebenen Vorgang nacheinander für seine Eingabe ausführt.</span><span class="sxs-lookup"><span data-stu-id="32a8a-111">A new operation that performs each given operation in sequence on its input.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="32a8a-112">Typparameter</span><span class="sxs-lookup"><span data-stu-id="32a8a-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="32a8a-113">GIF</span><span class="sxs-lookup"><span data-stu-id="32a8a-113">'T</span></span>

<span data-ttu-id="32a8a-114">Das Ziel, auf dem die einzelnen Vorgänge im Array agieren.</span><span class="sxs-lookup"><span data-stu-id="32a8a-114">The target on which each of the operations in the array act.</span></span>

## <a name="see-also"></a><span data-ttu-id="32a8a-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="32a8a-115">See Also</span></span>

- [<span data-ttu-id="32a8a-116">Microsoft. Quantum. Canon. Bound</span><span class="sxs-lookup"><span data-stu-id="32a8a-116">Microsoft.Quantum.Canon.Bound</span></span>](xref:Microsoft.Quantum.Canon.Bound)