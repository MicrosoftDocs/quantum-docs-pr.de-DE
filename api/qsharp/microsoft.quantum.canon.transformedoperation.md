---
uid: Microsoft.Quantum.Canon.TransformedOperation
title: Transformedoperation-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: TransformedOperation
qsharp.summary: Given a function and an operation, returns a new operation whose input is transformed by the given function.
ms.openlocfilehash: a26cc178f67fd99324355ac230d9e91081b6e238
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96204928"
---
# <a name="transformedoperation-function"></a><span data-ttu-id="324ed-102">Transformedoperation-Funktion</span><span class="sxs-lookup"><span data-stu-id="324ed-102">TransformedOperation function</span></span>

<span data-ttu-id="324ed-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="324ed-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="324ed-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="324ed-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="324ed-105">Gibt bei Angabe einer Funktion und eines Vorgangs einen neuen Vorgang zurück, dessen Eingabe von der angegebenen Funktion transformiert wird.</span><span class="sxs-lookup"><span data-stu-id="324ed-105">Given a function and an operation, returns a new operation whose input is transformed by the given function.</span></span>

```qsharp
function TransformedOperation<'T, 'U> (fn : ('U -> 'T), op : ('T => Unit)) : ('U => Unit)
```


## <a name="input"></a><span data-ttu-id="324ed-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="324ed-106">Input</span></span>

### <a name="fn--u---t"></a><span data-ttu-id="324ed-107">FN: ' U-> 't</span><span class="sxs-lookup"><span data-stu-id="324ed-107">fn : 'U -> 'T</span></span>

<span data-ttu-id="324ed-108">Eine Funktion, die die angegebene Eingabe in ein vom Vorgang erwartetes Formular umwandelt.</span><span class="sxs-lookup"><span data-stu-id="324ed-108">A function that transforms the given input into a form expected by the operation.</span></span>


### <a name="op--t--unit"></a><span data-ttu-id="324ed-109">OP: 't => [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="324ed-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="324ed-110">Der Vorgang, der transformiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="324ed-110">The operation to be transformed.</span></span>



## <a name="output--u--unit"></a><span data-ttu-id="324ed-111">Ausgabe: "U => [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="324ed-111">Output : 'U => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="324ed-112">Ein neuer Vorgang `fn` , den tbat mit seiner Eingabe aufruft, übergibt die resultierende Ausgabe anschließend an `op` .</span><span class="sxs-lookup"><span data-stu-id="324ed-112">A new operation tbat calls `fn` with its input, then passes the resulting output to `op`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="324ed-113">Typparameter</span><span class="sxs-lookup"><span data-stu-id="324ed-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="324ed-114">GIF</span><span class="sxs-lookup"><span data-stu-id="324ed-114">'T</span></span>


### <a name="u"></a><span data-ttu-id="324ed-115">"U</span><span class="sxs-lookup"><span data-stu-id="324ed-115">'U</span></span>



## <a name="see-also"></a><span data-ttu-id="324ed-116">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="324ed-116">See Also</span></span>

- [<span data-ttu-id="324ed-117">Microsoft. Quantum. Canon. transformedoperationa</span><span class="sxs-lookup"><span data-stu-id="324ed-117">Microsoft.Quantum.Canon.TransformedOperationA</span></span>](xref:Microsoft.Quantum.Canon.TransformedOperationA)
- [<span data-ttu-id="324ed-118">Microsoft. Quantum. Canon. transformedoperationc</span><span class="sxs-lookup"><span data-stu-id="324ed-118">Microsoft.Quantum.Canon.TransformedOperationC</span></span>](xref:Microsoft.Quantum.Canon.TransformedOperationC)
- [<span data-ttu-id="324ed-119">Microsoft. Quantum. Canon. transformedoperationca</span><span class="sxs-lookup"><span data-stu-id="324ed-119">Microsoft.Quantum.Canon.TransformedOperationCA</span></span>](xref:Microsoft.Quantum.Canon.TransformedOperationCA)
- [<span data-ttu-id="324ed-120">Microsoft. Quantum. Canon. applywithinputtransformation</span><span class="sxs-lookup"><span data-stu-id="324ed-120">Microsoft.Quantum.Canon.ApplyWithInputTransformation</span></span>](xref:Microsoft.Quantum.Canon.ApplyWithInputTransformation)
- [<span data-ttu-id="324ed-121">Microsoft. Quantum. Canon. verfasst</span><span class="sxs-lookup"><span data-stu-id="324ed-121">Microsoft.Quantum.Canon.Composed</span></span>](xref:Microsoft.Quantum.Canon.Composed)