---
uid: Microsoft.Quantum.Canon.TransformedOperationC
title: Transformedoperationc-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: TransformedOperationC
qsharp.summary: Given a function and an operation, returns a new operation whose input is transformed by the given function.
ms.openlocfilehash: 964576788bc80dd8920acdfb62d5d69a060e75f6
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96204860"
---
# <a name="transformedoperationc-function"></a><span data-ttu-id="ef3fc-102">Transformedoperationc-Funktion</span><span class="sxs-lookup"><span data-stu-id="ef3fc-102">TransformedOperationC function</span></span>

<span data-ttu-id="ef3fc-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="ef3fc-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="ef3fc-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="ef3fc-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="ef3fc-105">Gibt bei Angabe einer Funktion und eines Vorgangs einen neuen Vorgang zurück, dessen Eingabe von der angegebenen Funktion transformiert wird.</span><span class="sxs-lookup"><span data-stu-id="ef3fc-105">Given a function and an operation, returns a new operation whose input is transformed by the given function.</span></span>

```qsharp
function TransformedOperationC<'T, 'U> (fn : ('U -> 'T), op : ('T => Unit is Ctl)) : ('U => Unit is Ctl)
```


## <a name="input"></a><span data-ttu-id="ef3fc-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ef3fc-106">Input</span></span>

### <a name="fn--u---t"></a><span data-ttu-id="ef3fc-107">FN: ' U-> 't</span><span class="sxs-lookup"><span data-stu-id="ef3fc-107">fn : 'U -> 'T</span></span>

<span data-ttu-id="ef3fc-108">Eine Funktion, die die angegebene Eingabe in ein vom Vorgang erwartetes Formular umwandelt.</span><span class="sxs-lookup"><span data-stu-id="ef3fc-108">A function that transforms the given input into a form expected by the operation.</span></span>


### <a name="op--t--unit--is-ctl"></a><span data-ttu-id="ef3fc-109">OP: 't => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist CTL</span><span class="sxs-lookup"><span data-stu-id="ef3fc-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="ef3fc-110">Der Vorgang, der transformiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="ef3fc-110">The operation to be transformed.</span></span>



## <a name="output--u--unit--is-ctl"></a><span data-ttu-id="ef3fc-111">Ausgabe: "U => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist CTL</span><span class="sxs-lookup"><span data-stu-id="ef3fc-111">Output : 'U => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="ef3fc-112">Ein neuer Vorgang `fn` , den tbat mit seiner Eingabe aufruft, übergibt die resultierende Ausgabe anschließend an `op` .</span><span class="sxs-lookup"><span data-stu-id="ef3fc-112">A new operation tbat calls `fn` with its input, then passes the resulting output to `op`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="ef3fc-113">Typparameter</span><span class="sxs-lookup"><span data-stu-id="ef3fc-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="ef3fc-114">GIF</span><span class="sxs-lookup"><span data-stu-id="ef3fc-114">'T</span></span>


### <a name="u"></a><span data-ttu-id="ef3fc-115">"U</span><span class="sxs-lookup"><span data-stu-id="ef3fc-115">'U</span></span>



## <a name="see-also"></a><span data-ttu-id="ef3fc-116">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ef3fc-116">See Also</span></span>

- [<span data-ttu-id="ef3fc-117">Microsoft. Quantum. Canon. transformedoperation</span><span class="sxs-lookup"><span data-stu-id="ef3fc-117">Microsoft.Quantum.Canon.TransformedOperation</span></span>](xref:Microsoft.Quantum.Canon.TransformedOperation)
- [<span data-ttu-id="ef3fc-118">Microsoft. Quantum. Canon. transformedoperationa</span><span class="sxs-lookup"><span data-stu-id="ef3fc-118">Microsoft.Quantum.Canon.TransformedOperationA</span></span>](xref:Microsoft.Quantum.Canon.TransformedOperationA)
- [<span data-ttu-id="ef3fc-119">Microsoft. Quantum. Canon. transformedoperationca</span><span class="sxs-lookup"><span data-stu-id="ef3fc-119">Microsoft.Quantum.Canon.TransformedOperationCA</span></span>](xref:Microsoft.Quantum.Canon.TransformedOperationCA)
- [<span data-ttu-id="ef3fc-120">Microsoft. Quantum. Canon. applywithinputtransformation</span><span class="sxs-lookup"><span data-stu-id="ef3fc-120">Microsoft.Quantum.Canon.ApplyWithInputTransformation</span></span>](xref:Microsoft.Quantum.Canon.ApplyWithInputTransformation)
- [<span data-ttu-id="ef3fc-121">Microsoft. Quantum. Canon. verfasst</span><span class="sxs-lookup"><span data-stu-id="ef3fc-121">Microsoft.Quantum.Canon.Composed</span></span>](xref:Microsoft.Quantum.Canon.Composed)