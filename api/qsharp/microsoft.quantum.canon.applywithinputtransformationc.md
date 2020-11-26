---
uid: Microsoft.Quantum.Canon.ApplyWithInputTransformationC
title: Applywithinputtransformationc-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyWithInputTransformationC
qsharp.summary: Given an operation that accepts some input, a function that returns an output compatible with that operation, and an input to that function, applies the operation using the function to transform the input to a form expected by the operation.
ms.openlocfilehash: 030c41d3ce0a5d613a95c6511f7278497ec5cda1
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96217168"
---
# <a name="applywithinputtransformationc-operation"></a><span data-ttu-id="efb4f-102">Applywithinputtransformationc-Vorgang</span><span class="sxs-lookup"><span data-stu-id="efb4f-102">ApplyWithInputTransformationC operation</span></span>

<span data-ttu-id="efb4f-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="efb4f-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="efb4f-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="efb4f-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="efb4f-105">Bei einem Vorgang, der eine Eingabe akzeptiert, eine Funktion, die eine mit diesem Vorgang kompatible Ausgabe zurückgibt, sowie eine Eingabe für diese Funktion wendet den Vorgang mithilfe der-Funktion an, um die Eingabe in ein vom Vorgang erwartetes Formular umzuwandeln.</span><span class="sxs-lookup"><span data-stu-id="efb4f-105">Given an operation that accepts some input, a function that returns an output compatible with that operation, and an input to that function, applies the operation using the function to transform the input to a form expected by the operation.</span></span>

```qsharp
operation ApplyWithInputTransformationC<'T, 'U> (fn : ('U -> 'T), op : ('T => Unit is Ctl), input : 'U) : Unit is Ctl
```


## <a name="input"></a><span data-ttu-id="efb4f-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="efb4f-106">Input</span></span>

### <a name="fn--u---t"></a><span data-ttu-id="efb4f-107">FN: ' U-> 't</span><span class="sxs-lookup"><span data-stu-id="efb4f-107">fn : 'U -> 'T</span></span>

<span data-ttu-id="efb4f-108">Eine Funktion, die die angegebene Eingabe in ein vom Vorgang erwartetes Formular umwandelt.</span><span class="sxs-lookup"><span data-stu-id="efb4f-108">A function that transforms the given input into a form expected by the operation.</span></span>


### <a name="op--t--unit--is-ctl"></a><span data-ttu-id="efb4f-109">OP: 't => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist CTL</span><span class="sxs-lookup"><span data-stu-id="efb4f-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="efb4f-110">Der anzuwendende Vorgang.</span><span class="sxs-lookup"><span data-stu-id="efb4f-110">The operation to be applied.</span></span>


### <a name="input--u"></a><span data-ttu-id="efb4f-111">Eingabe: "U</span><span class="sxs-lookup"><span data-stu-id="efb4f-111">input : 'U</span></span>

<span data-ttu-id="efb4f-112">Eine Eingabe für die Funktion.</span><span class="sxs-lookup"><span data-stu-id="efb4f-112">An input to the function.</span></span>



## <a name="output--unit"></a><span data-ttu-id="efb4f-113">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="efb4f-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="efb4f-114">Typparameter</span><span class="sxs-lookup"><span data-stu-id="efb4f-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="efb4f-115">GIF</span><span class="sxs-lookup"><span data-stu-id="efb4f-115">'T</span></span>


### <a name="u"></a><span data-ttu-id="efb4f-116">"U</span><span class="sxs-lookup"><span data-stu-id="efb4f-116">'U</span></span>



## <a name="see-also"></a><span data-ttu-id="efb4f-117">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="efb4f-117">See Also</span></span>

- [<span data-ttu-id="efb4f-118">Microsoft. Quantum. Canon. applywithinputtransformation</span><span class="sxs-lookup"><span data-stu-id="efb4f-118">Microsoft.Quantum.Canon.ApplyWithInputTransformation</span></span>](xref:Microsoft.Quantum.Canon.ApplyWithInputTransformation)
- [<span data-ttu-id="efb4f-119">Microsoft. Quantum. Canon. applywithinputtransformationa</span><span class="sxs-lookup"><span data-stu-id="efb4f-119">Microsoft.Quantum.Canon.ApplyWithInputTransformationA</span></span>](xref:Microsoft.Quantum.Canon.ApplyWithInputTransformationA)
- [<span data-ttu-id="efb4f-120">Microsoft. Quantum. Canon. applywithinputtransformationca</span><span class="sxs-lookup"><span data-stu-id="efb4f-120">Microsoft.Quantum.Canon.ApplyWithInputTransformationCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyWithInputTransformationCA)
- [<span data-ttu-id="efb4f-121">Microsoft. Quantum. Canon. transformedoperation</span><span class="sxs-lookup"><span data-stu-id="efb4f-121">Microsoft.Quantum.Canon.TransformedOperation</span></span>](xref:Microsoft.Quantum.Canon.TransformedOperation)