---
uid: Microsoft.Quantum.Canon.BoundCA
title: Boundca-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: BoundCA
qsharp.summary: Given an array of operations acting on a single input, produces a new operation that performs each given operation in sequence. The modifier `CA` indicates that all operations in the array are adjointable and controllable.
ms.openlocfilehash: 391183829a3cc8b7aa8051767dcfc6bec9638223
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98844531"
---
# <a name="boundca-function"></a><span data-ttu-id="8e26b-102">Boundca-Funktion</span><span class="sxs-lookup"><span data-stu-id="8e26b-102">BoundCA function</span></span>

<span data-ttu-id="8e26b-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="8e26b-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="8e26b-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="8e26b-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="8e26b-105">Bei einem Array von Vorgängen, die für eine einzelne Eingabe agieren, erzeugt einen neuen Vorgang, der jeden gegebenen Vorgang nacheinander ausführt.</span><span class="sxs-lookup"><span data-stu-id="8e26b-105">Given an array of operations acting on a single input, produces a new operation that performs each given operation in sequence.</span></span>
<span data-ttu-id="8e26b-106">Der-Modifizierer `CA` gibt an, dass alle Vorgänge im Array adjointable und steuerbar sind.</span><span class="sxs-lookup"><span data-stu-id="8e26b-106">The modifier `CA` indicates that all operations in the array are adjointable and controllable.</span></span>

```qsharp
function BoundCA<'T> (operations : ('T => Unit is Adj + Ctl)[]) : ('T => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="8e26b-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8e26b-107">Input</span></span>

### <a name="operations--t--unit--is-adj--ctl"></a><span data-ttu-id="8e26b-108">Vorgänge: 't => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL []</span><span class="sxs-lookup"><span data-stu-id="8e26b-108">operations : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl[]</span></span>

<span data-ttu-id="8e26b-109">Eine Sequenz von Vorgängen, die für eine angegebene Eingabe ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="8e26b-109">A sequence of operations to be performed on a given input.</span></span>



## <a name="output--t--unit--is-adj--ctl"></a><span data-ttu-id="8e26b-110">Ausgabe: 't => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="8e26b-110">Output : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="8e26b-111">Ein neuer Vorgang, der jeden gegebenen Vorgang nacheinander für seine Eingabe ausführt.</span><span class="sxs-lookup"><span data-stu-id="8e26b-111">A new operation that performs each given operation in sequence on its input.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="8e26b-112">Typparameter</span><span class="sxs-lookup"><span data-stu-id="8e26b-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="8e26b-113">GIF</span><span class="sxs-lookup"><span data-stu-id="8e26b-113">'T</span></span>

<span data-ttu-id="8e26b-114">Das Ziel, auf dem die einzelnen Vorgänge im Array agieren.</span><span class="sxs-lookup"><span data-stu-id="8e26b-114">The target on which each of the operations in the array act.</span></span>

## <a name="example"></a><span data-ttu-id="8e26b-115">Beispiel</span><span class="sxs-lookup"><span data-stu-id="8e26b-115">Example</span></span>

<span data-ttu-id="8e26b-116">Die folgenden sind gleichwertig:</span><span class="sxs-lookup"><span data-stu-id="8e26b-116">The following are equivalent:</span></span>

```qsharp
let bound = BoundCA([U, V]);
bound(x);
```

<span data-ttu-id="8e26b-117">and</span><span class="sxs-lookup"><span data-stu-id="8e26b-117">and</span></span>

```qsharp
U(x); V(x);
```

## <a name="see-also"></a><span data-ttu-id="8e26b-118">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="8e26b-118">See Also</span></span>

- [<span data-ttu-id="8e26b-119">Microsoft. Quantum. Canon. Bound</span><span class="sxs-lookup"><span data-stu-id="8e26b-119">Microsoft.Quantum.Canon.Bound</span></span>](xref:Microsoft.Quantum.Canon.Bound)