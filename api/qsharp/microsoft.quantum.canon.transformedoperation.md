---
uid: Microsoft.Quantum.Canon.TransformedOperation
title: Transformedoperation-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: TransformedOperation
qsharp.summary: Given a function and an operation, returns a new operation whose input is transformed by the given function.
ms.openlocfilehash: d8c2f52290ce89d0a8ff138ba25f6b2e5e0516d5
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703769"
---
# <a name="transformedoperation-function"></a><span data-ttu-id="a8983-102">Transformedoperation-Funktion</span><span class="sxs-lookup"><span data-stu-id="a8983-102">TransformedOperation function</span></span>

<span data-ttu-id="a8983-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="a8983-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="a8983-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="a8983-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="a8983-105">Gibt bei Angabe einer Funktion und eines Vorgangs einen neuen Vorgang zurück, dessen Eingabe von der angegebenen Funktion transformiert wird.</span><span class="sxs-lookup"><span data-stu-id="a8983-105">Given a function and an operation, returns a new operation whose input is transformed by the given function.</span></span>

```qsharp
function TransformedOperation<'T, 'U> (fn : ('U -> 'T), op : ('T => Unit)) : ('U => Unit)
```


## <a name="input"></a><span data-ttu-id="a8983-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a8983-106">Input</span></span>

### <a name="fn--u---t"></a><span data-ttu-id="a8983-107">FN: ' U-> 't</span><span class="sxs-lookup"><span data-stu-id="a8983-107">fn : 'U -> 'T</span></span>

<span data-ttu-id="a8983-108">Eine Funktion, die die angegebene Eingabe in ein vom Vorgang erwartetes Formular umwandelt.</span><span class="sxs-lookup"><span data-stu-id="a8983-108">A function that transforms the given input into a form expected by the operation.</span></span>


### <a name="op--t--unit"></a><span data-ttu-id="a8983-109">OP: 't => [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="a8983-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="a8983-110">Der Vorgang, der transformiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="a8983-110">The operation to be transformed.</span></span>



## <a name="output--u--unit"></a><span data-ttu-id="a8983-111">Ausgabe: "U => [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="a8983-111">Output : 'U => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="a8983-112">Ein neuer Vorgang `fn` , den tbat mit seiner Eingabe aufruft, übergibt die resultierende Ausgabe anschließend an `op` .</span><span class="sxs-lookup"><span data-stu-id="a8983-112">A new operation tbat calls `fn` with its input, then passes the resulting output to `op`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="a8983-113">Typparameter</span><span class="sxs-lookup"><span data-stu-id="a8983-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="a8983-114">GIF</span><span class="sxs-lookup"><span data-stu-id="a8983-114">'T</span></span>


### <a name="u"></a><span data-ttu-id="a8983-115">"U</span><span class="sxs-lookup"><span data-stu-id="a8983-115">'U</span></span>



## <a name="see-also"></a><span data-ttu-id="a8983-116">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="a8983-116">See Also</span></span>

- [<span data-ttu-id="a8983-117">Microsoft. Quantum. Canon. transformedoperationa</span><span class="sxs-lookup"><span data-stu-id="a8983-117">Microsoft.Quantum.Canon.TransformedOperationA</span></span>](xref:Microsoft.Quantum.Canon.TransformedOperationA)
- [<span data-ttu-id="a8983-118">Microsoft. Quantum. Canon. transformedoperationc</span><span class="sxs-lookup"><span data-stu-id="a8983-118">Microsoft.Quantum.Canon.TransformedOperationC</span></span>](xref:Microsoft.Quantum.Canon.TransformedOperationC)
- [<span data-ttu-id="a8983-119">Microsoft. Quantum. Canon. transformedoperationca</span><span class="sxs-lookup"><span data-stu-id="a8983-119">Microsoft.Quantum.Canon.TransformedOperationCA</span></span>](xref:Microsoft.Quantum.Canon.TransformedOperationCA)
- [<span data-ttu-id="a8983-120">Microsoft. Quantum. Canon. applywithinputtransformation</span><span class="sxs-lookup"><span data-stu-id="a8983-120">Microsoft.Quantum.Canon.ApplyWithInputTransformation</span></span>](xref:Microsoft.Quantum.Canon.ApplyWithInputTransformation)
- [<span data-ttu-id="a8983-121">Microsoft. Quantum. Canon. verfasst</span><span class="sxs-lookup"><span data-stu-id="a8983-121">Microsoft.Quantum.Canon.Composed</span></span>](xref:Microsoft.Quantum.Canon.Composed)