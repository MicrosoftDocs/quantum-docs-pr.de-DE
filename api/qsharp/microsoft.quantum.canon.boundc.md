---
uid: Microsoft.Quantum.Canon.BoundC
title: Boundc-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: BoundC
qsharp.summary: Given an array of operations acting on a single input, produces a new operation that performs each given operation in sequence. The modifier `C` indicates that all operations in the array are controllable.
ms.openlocfilehash: 02e9b6a9676cdd1996d3a2413b2a6383e3a4e90e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96207580"
---
# <a name="boundc-function"></a><span data-ttu-id="5505f-102">Boundc-Funktion</span><span class="sxs-lookup"><span data-stu-id="5505f-102">BoundC function</span></span>

<span data-ttu-id="5505f-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="5505f-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="5505f-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="5505f-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="5505f-105">Bei einem Array von Vorgängen, die für eine einzelne Eingabe agieren, erzeugt einen neuen Vorgang, der jeden gegebenen Vorgang nacheinander ausführt.</span><span class="sxs-lookup"><span data-stu-id="5505f-105">Given an array of operations acting on a single input, produces a new operation that performs each given operation in sequence.</span></span>
<span data-ttu-id="5505f-106">Der-Modifizierer `C` gibt an, dass alle Vorgänge im Array steuerbar sind.</span><span class="sxs-lookup"><span data-stu-id="5505f-106">The modifier `C` indicates that all operations in the array are controllable.</span></span>

```qsharp
function BoundC<'T> (operations : ('T => Unit is Ctl)[]) : ('T => Unit is Ctl)
```


## <a name="input"></a><span data-ttu-id="5505f-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5505f-107">Input</span></span>

### <a name="operations--t--unit--is-ctl"></a><span data-ttu-id="5505f-108">Vorgänge: 't => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist CTL []</span><span class="sxs-lookup"><span data-stu-id="5505f-108">operations : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl[]</span></span>

<span data-ttu-id="5505f-109">Eine Sequenz von Vorgängen, die für eine angegebene Eingabe ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="5505f-109">A sequence of operations to be performed on a given input.</span></span>



## <a name="output--t--unit--is-ctl"></a><span data-ttu-id="5505f-110">Ausgabe: 't => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist CTL</span><span class="sxs-lookup"><span data-stu-id="5505f-110">Output : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="5505f-111">Ein neuer Vorgang, der jeden gegebenen Vorgang nacheinander für seine Eingabe ausführt.</span><span class="sxs-lookup"><span data-stu-id="5505f-111">A new operation that performs each given operation in sequence on its input.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="5505f-112">Typparameter</span><span class="sxs-lookup"><span data-stu-id="5505f-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="5505f-113">GIF</span><span class="sxs-lookup"><span data-stu-id="5505f-113">'T</span></span>

<span data-ttu-id="5505f-114">Das Ziel, auf dem die einzelnen Vorgänge im Array agieren.</span><span class="sxs-lookup"><span data-stu-id="5505f-114">The target on which each of the operations in the array act.</span></span>

## <a name="see-also"></a><span data-ttu-id="5505f-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="5505f-115">See Also</span></span>

- [<span data-ttu-id="5505f-116">Microsoft. Quantum. Canon. Bound</span><span class="sxs-lookup"><span data-stu-id="5505f-116">Microsoft.Quantum.Canon.Bound</span></span>](xref:Microsoft.Quantum.Canon.Bound)