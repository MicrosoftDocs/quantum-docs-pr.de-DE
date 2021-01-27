---
uid: Microsoft.Quantum.Canon.ApplyWithInputTransformation
title: Applywithinputtransformation-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyWithInputTransformation
qsharp.summary: Given an operation that accepts some input, a function that returns an output compatible with that operation, and an input to that function, applies the operation using the function to transform the input to a form expected by the operation.
ms.openlocfilehash: d4589acbe9f9dc6c6ab665582ed663dbc193edbb
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850376"
---
# <a name="applywithinputtransformation-operation"></a><span data-ttu-id="d0e47-102">Applywithinputtransformation-Vorgang</span><span class="sxs-lookup"><span data-stu-id="d0e47-102">ApplyWithInputTransformation operation</span></span>

<span data-ttu-id="d0e47-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="d0e47-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="d0e47-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="d0e47-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="d0e47-105">Bei einem Vorgang, der eine Eingabe akzeptiert, eine Funktion, die eine mit diesem Vorgang kompatible Ausgabe zurückgibt, sowie eine Eingabe für diese Funktion wendet den Vorgang mithilfe der-Funktion an, um die Eingabe in ein vom Vorgang erwartetes Formular umzuwandeln.</span><span class="sxs-lookup"><span data-stu-id="d0e47-105">Given an operation that accepts some input, a function that returns an output compatible with that operation, and an input to that function, applies the operation using the function to transform the input to a form expected by the operation.</span></span>

```qsharp
operation ApplyWithInputTransformation<'T, 'U> (fn : ('U -> 'T), op : ('T => Unit), input : 'U) : Unit
```


## <a name="input"></a><span data-ttu-id="d0e47-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d0e47-106">Input</span></span>

### <a name="fn--u---t"></a><span data-ttu-id="d0e47-107">FN: ' U-> 't</span><span class="sxs-lookup"><span data-stu-id="d0e47-107">fn : 'U -> 'T</span></span>

<span data-ttu-id="d0e47-108">Eine Funktion, die die angegebene Eingabe in ein vom Vorgang erwartetes Formular umwandelt.</span><span class="sxs-lookup"><span data-stu-id="d0e47-108">A function that transforms the given input into a form expected by the operation.</span></span>


### <a name="op--t--unit"></a><span data-ttu-id="d0e47-109">OP: 't => [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="d0e47-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="d0e47-110">Der anzuwendende Vorgang.</span><span class="sxs-lookup"><span data-stu-id="d0e47-110">The operation to be applied.</span></span>


### <a name="input--u"></a><span data-ttu-id="d0e47-111">Eingabe: "U</span><span class="sxs-lookup"><span data-stu-id="d0e47-111">input : 'U</span></span>

<span data-ttu-id="d0e47-112">Eine Eingabe für die Funktion.</span><span class="sxs-lookup"><span data-stu-id="d0e47-112">An input to the function.</span></span>



## <a name="output--unit"></a><span data-ttu-id="d0e47-113">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="d0e47-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="d0e47-114">Typparameter</span><span class="sxs-lookup"><span data-stu-id="d0e47-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="d0e47-115">GIF</span><span class="sxs-lookup"><span data-stu-id="d0e47-115">'T</span></span>


### <a name="u"></a><span data-ttu-id="d0e47-116">"U</span><span class="sxs-lookup"><span data-stu-id="d0e47-116">'U</span></span>



## <a name="example"></a><span data-ttu-id="d0e47-117">Beispiel</span><span class="sxs-lookup"><span data-stu-id="d0e47-117">Example</span></span>

<span data-ttu-id="d0e47-118">Der folgende-Befehl verwendet @"Microsoft.Quantum.Arithmetic.LittleEndianAsBigEndian" , um einen für Eingaben entworfenen Vorgang @"Microsoft.Quantum.Arithmetic.BigEndian" auf eine Eingabe des Typs anzuwenden @"Microsoft.Quantum.Arithmetic.LittleEndian" :</span><span class="sxs-lookup"><span data-stu-id="d0e47-118">The following call uses @"Microsoft.Quantum.Arithmetic.LittleEndianAsBigEndian" to apply an operation designed for @"Microsoft.Quantum.Arithmetic.BigEndian" inputs to an input of type @"Microsoft.Quantum.Arithmetic.LittleEndian":</span></span>

```qsharp
ApplyWithInputTransformation(LittleEndianAsBigEndian, ApplyXorInPlaceBE, LittleEndian(qubits));
```

## <a name="see-also"></a><span data-ttu-id="d0e47-119">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="d0e47-119">See Also</span></span>

- [<span data-ttu-id="d0e47-120">Microsoft. Quantum. Canon. applywithinputtransformationa</span><span class="sxs-lookup"><span data-stu-id="d0e47-120">Microsoft.Quantum.Canon.ApplyWithInputTransformationA</span></span>](xref:Microsoft.Quantum.Canon.ApplyWithInputTransformationA)
- [<span data-ttu-id="d0e47-121">Microsoft. Quantum. Canon. applywithinputtransformationc</span><span class="sxs-lookup"><span data-stu-id="d0e47-121">Microsoft.Quantum.Canon.ApplyWithInputTransformationC</span></span>](xref:Microsoft.Quantum.Canon.ApplyWithInputTransformationC)
- [<span data-ttu-id="d0e47-122">Microsoft. Quantum. Canon. applywithinputtransformationca</span><span class="sxs-lookup"><span data-stu-id="d0e47-122">Microsoft.Quantum.Canon.ApplyWithInputTransformationCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyWithInputTransformationCA)
- [<span data-ttu-id="d0e47-123">Microsoft. Quantum. Canon. transformedoperation</span><span class="sxs-lookup"><span data-stu-id="d0e47-123">Microsoft.Quantum.Canon.TransformedOperation</span></span>](xref:Microsoft.Quantum.Canon.TransformedOperation)