---
uid: Microsoft.Quantum.Canon.Bound
title: Gebundene Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Bound
qsharp.summary: Given an array of operations acting on a single input, produces a new operation that performs each given operation in sequence.
ms.openlocfilehash: 041f654c14f6e926d60038fee698b2b829fab8b3
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841067"
---
# <a name="bound-function"></a><span data-ttu-id="439ef-102">Gebundene Funktion</span><span class="sxs-lookup"><span data-stu-id="439ef-102">Bound function</span></span>

<span data-ttu-id="439ef-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="439ef-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="439ef-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="439ef-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="439ef-105">Bei einem Array von Vorgängen, die für eine einzelne Eingabe agieren, erzeugt einen neuen Vorgang, der jeden gegebenen Vorgang nacheinander ausführt.</span><span class="sxs-lookup"><span data-stu-id="439ef-105">Given an array of operations acting on a single input, produces a new operation that performs each given operation in sequence.</span></span>

```qsharp
function Bound<'T> (operations : ('T => Unit)[]) : ('T => Unit)
```


## <a name="input"></a><span data-ttu-id="439ef-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="439ef-106">Input</span></span>

### <a name="operations--t--unit-"></a><span data-ttu-id="439ef-107">Vorgänge: 't => [Unit](xref:microsoft.quantum.lang-ref.unit) []</span><span class="sxs-lookup"><span data-stu-id="439ef-107">operations : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) []</span></span>

<span data-ttu-id="439ef-108">Eine Sequenz von Vorgängen, die für eine angegebene Eingabe ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="439ef-108">A sequence of operations to be performed on a given input.</span></span>



## <a name="output--t--unit"></a><span data-ttu-id="439ef-109">Ausgabe: 't => [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="439ef-109">Output : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="439ef-110">Ein neuer Vorgang, der jeden gegebenen Vorgang nacheinander für seine Eingabe ausführt.</span><span class="sxs-lookup"><span data-stu-id="439ef-110">A new operation that performs each given operation in sequence on its input.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="439ef-111">Typparameter</span><span class="sxs-lookup"><span data-stu-id="439ef-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="439ef-112">GIF</span><span class="sxs-lookup"><span data-stu-id="439ef-112">'T</span></span>

<span data-ttu-id="439ef-113">Das Ziel, auf dem die einzelnen Vorgänge im Array agieren.</span><span class="sxs-lookup"><span data-stu-id="439ef-113">The target on which each of the operations in the array act.</span></span>

## <a name="example"></a><span data-ttu-id="439ef-114">Beispiel</span><span class="sxs-lookup"><span data-stu-id="439ef-114">Example</span></span>

<span data-ttu-id="439ef-115">Die folgenden sind gleichwertig:</span><span class="sxs-lookup"><span data-stu-id="439ef-115">The following are equivalent:</span></span>

```qsharp
let bound = Bound([U, V]);
bound(x);
```

<span data-ttu-id="439ef-116">and</span><span class="sxs-lookup"><span data-stu-id="439ef-116">and</span></span>

```qsharp
U(x); V(x);
```

## <a name="see-also"></a><span data-ttu-id="439ef-117">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="439ef-117">See Also</span></span>

- [<span data-ttu-id="439ef-118">Microsoft. Quantum. Canon. boundc</span><span class="sxs-lookup"><span data-stu-id="439ef-118">Microsoft.Quantum.Canon.BoundC</span></span>](xref:Microsoft.Quantum.Canon.BoundC)
- [<span data-ttu-id="439ef-119">Microsoft. Quantum. Canon. bounda</span><span class="sxs-lookup"><span data-stu-id="439ef-119">Microsoft.Quantum.Canon.BoundA</span></span>](xref:Microsoft.Quantum.Canon.BoundA)
- [<span data-ttu-id="439ef-120">Microsoft. Quantum. Canon. boundca</span><span class="sxs-lookup"><span data-stu-id="439ef-120">Microsoft.Quantum.Canon.BoundCA</span></span>](xref:Microsoft.Quantum.Canon.BoundCA)