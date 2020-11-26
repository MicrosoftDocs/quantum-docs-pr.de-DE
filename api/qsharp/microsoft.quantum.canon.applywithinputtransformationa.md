---
uid: Microsoft.Quantum.Canon.ApplyWithInputTransformationA
title: Applywithinputtransformationa-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyWithInputTransformationA
qsharp.summary: Given an operation that accepts some input, a function that returns an output compatible with that operation, and an input to that function, applies the operation using the function to transform the input to a form expected by the operation.
ms.openlocfilehash: 8d65af33a0bc8ce3c08da54b34e68b4e22b710ca
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96207886"
---
# <a name="applywithinputtransformationa-operation"></a><span data-ttu-id="7afed-102">Applywithinputtransformationa-Vorgang</span><span class="sxs-lookup"><span data-stu-id="7afed-102">ApplyWithInputTransformationA operation</span></span>

<span data-ttu-id="7afed-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="7afed-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="7afed-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="7afed-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="7afed-105">Bei einem Vorgang, der eine Eingabe akzeptiert, eine Funktion, die eine mit diesem Vorgang kompatible Ausgabe zurückgibt, sowie eine Eingabe für diese Funktion wendet den Vorgang mithilfe der-Funktion an, um die Eingabe in ein vom Vorgang erwartetes Formular umzuwandeln.</span><span class="sxs-lookup"><span data-stu-id="7afed-105">Given an operation that accepts some input, a function that returns an output compatible with that operation, and an input to that function, applies the operation using the function to transform the input to a form expected by the operation.</span></span>

```qsharp
operation ApplyWithInputTransformationA<'T, 'U> (fn : ('U -> 'T), op : ('T => Unit is Adj), input : 'U) : Unit is Adj
```


## <a name="input"></a><span data-ttu-id="7afed-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="7afed-106">Input</span></span>

### <a name="fn--u---t"></a><span data-ttu-id="7afed-107">FN: ' U-> 't</span><span class="sxs-lookup"><span data-stu-id="7afed-107">fn : 'U -> 'T</span></span>

<span data-ttu-id="7afed-108">Eine Funktion, die die angegebene Eingabe in ein vom Vorgang erwartetes Formular umwandelt.</span><span class="sxs-lookup"><span data-stu-id="7afed-108">A function that transforms the given input into a form expected by the operation.</span></span>


### <a name="op--t--unit--is-adj"></a><span data-ttu-id="7afed-109">OP: 't => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ</span><span class="sxs-lookup"><span data-stu-id="7afed-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="7afed-110">Der anzuwendende Vorgang.</span><span class="sxs-lookup"><span data-stu-id="7afed-110">The operation to be applied.</span></span>


### <a name="input--u"></a><span data-ttu-id="7afed-111">Eingabe: "U</span><span class="sxs-lookup"><span data-stu-id="7afed-111">input : 'U</span></span>

<span data-ttu-id="7afed-112">Eine Eingabe für die Funktion.</span><span class="sxs-lookup"><span data-stu-id="7afed-112">An input to the function.</span></span>



## <a name="output--unit"></a><span data-ttu-id="7afed-113">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="7afed-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="7afed-114">Typparameter</span><span class="sxs-lookup"><span data-stu-id="7afed-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="7afed-115">GIF</span><span class="sxs-lookup"><span data-stu-id="7afed-115">'T</span></span>


### <a name="u"></a><span data-ttu-id="7afed-116">"U</span><span class="sxs-lookup"><span data-stu-id="7afed-116">'U</span></span>



## <a name="see-also"></a><span data-ttu-id="7afed-117">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="7afed-117">See Also</span></span>

- [<span data-ttu-id="7afed-118">Microsoft. Quantum. Canon. applywithinputtransformation</span><span class="sxs-lookup"><span data-stu-id="7afed-118">Microsoft.Quantum.Canon.ApplyWithInputTransformation</span></span>](xref:Microsoft.Quantum.Canon.ApplyWithInputTransformation)
- [<span data-ttu-id="7afed-119">Microsoft. Quantum. Canon. applywithinputtransformationc</span><span class="sxs-lookup"><span data-stu-id="7afed-119">Microsoft.Quantum.Canon.ApplyWithInputTransformationC</span></span>](xref:Microsoft.Quantum.Canon.ApplyWithInputTransformationC)
- [<span data-ttu-id="7afed-120">Microsoft. Quantum. Canon. applywithinputtransformationca</span><span class="sxs-lookup"><span data-stu-id="7afed-120">Microsoft.Quantum.Canon.ApplyWithInputTransformationCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyWithInputTransformationCA)
- [<span data-ttu-id="7afed-121">Microsoft. Quantum. Canon. transformedoperation</span><span class="sxs-lookup"><span data-stu-id="7afed-121">Microsoft.Quantum.Canon.TransformedOperation</span></span>](xref:Microsoft.Quantum.Canon.TransformedOperation)