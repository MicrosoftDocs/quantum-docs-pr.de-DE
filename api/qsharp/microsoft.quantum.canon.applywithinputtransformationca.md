---
uid: Microsoft.Quantum.Canon.ApplyWithInputTransformationCA
title: Applywithinputtransformationca-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyWithInputTransformationCA
qsharp.summary: Given an operation that accepts some input, a function that returns an output compatible with that operation, and an input to that function, applies the operation using the function to transform the input to a form expected by the operation.
ms.openlocfilehash: b31ed1b3da0d5467588f4cb2e4368e68f0dbe9d5
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841117"
---
# <a name="applywithinputtransformationca-operation"></a><span data-ttu-id="ed8bb-102">Applywithinputtransformationca-Vorgang</span><span class="sxs-lookup"><span data-stu-id="ed8bb-102">ApplyWithInputTransformationCA operation</span></span>

<span data-ttu-id="ed8bb-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="ed8bb-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="ed8bb-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="ed8bb-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="ed8bb-105">Bei einem Vorgang, der eine Eingabe akzeptiert, eine Funktion, die eine mit diesem Vorgang kompatible Ausgabe zurückgibt, sowie eine Eingabe für diese Funktion wendet den Vorgang mithilfe der-Funktion an, um die Eingabe in ein vom Vorgang erwartetes Formular umzuwandeln.</span><span class="sxs-lookup"><span data-stu-id="ed8bb-105">Given an operation that accepts some input, a function that returns an output compatible with that operation, and an input to that function, applies the operation using the function to transform the input to a form expected by the operation.</span></span>

```qsharp
operation ApplyWithInputTransformationCA<'T, 'U> (fn : ('U -> 'T), op : ('T => Unit is Adj + Ctl), input : 'U) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="ed8bb-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ed8bb-106">Input</span></span>

### <a name="fn--u---t"></a><span data-ttu-id="ed8bb-107">FN: ' U-> 't</span><span class="sxs-lookup"><span data-stu-id="ed8bb-107">fn : 'U -> 'T</span></span>

<span data-ttu-id="ed8bb-108">Eine Funktion, die die angegebene Eingabe in ein vom Vorgang erwartetes Formular umwandelt.</span><span class="sxs-lookup"><span data-stu-id="ed8bb-108">A function that transforms the given input into a form expected by the operation.</span></span>


### <a name="op--t--unit--is-adj--ctl"></a><span data-ttu-id="ed8bb-109">OP: 't => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="ed8bb-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="ed8bb-110">Der anzuwendende Vorgang.</span><span class="sxs-lookup"><span data-stu-id="ed8bb-110">The operation to be applied.</span></span>


### <a name="input--u"></a><span data-ttu-id="ed8bb-111">Eingabe: "U</span><span class="sxs-lookup"><span data-stu-id="ed8bb-111">input : 'U</span></span>

<span data-ttu-id="ed8bb-112">Eine Eingabe für die Funktion.</span><span class="sxs-lookup"><span data-stu-id="ed8bb-112">An input to the function.</span></span>



## <a name="output--unit"></a><span data-ttu-id="ed8bb-113">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="ed8bb-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="ed8bb-114">Typparameter</span><span class="sxs-lookup"><span data-stu-id="ed8bb-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="ed8bb-115">GIF</span><span class="sxs-lookup"><span data-stu-id="ed8bb-115">'T</span></span>


### <a name="u"></a><span data-ttu-id="ed8bb-116">"U</span><span class="sxs-lookup"><span data-stu-id="ed8bb-116">'U</span></span>



## <a name="example"></a><span data-ttu-id="ed8bb-117">Beispiel</span><span class="sxs-lookup"><span data-stu-id="ed8bb-117">Example</span></span>

<span data-ttu-id="ed8bb-118">Der folgende-Befehl verwendet @"Microsoft.Quantum.Arithmetic.LittleEndianAsBigEndian" , um einen für Eingaben entworfenen Vorgang @"Microsoft.Quantum.Arithmetic.BigEndian" auf eine Eingabe des Typs anzuwenden @"Microsoft.Quantum.Arithmetic.LittleEndian" :</span><span class="sxs-lookup"><span data-stu-id="ed8bb-118">The following call uses @"Microsoft.Quantum.Arithmetic.LittleEndianAsBigEndian" to apply an operation designed for @"Microsoft.Quantum.Arithmetic.BigEndian" inputs to an input of type @"Microsoft.Quantum.Arithmetic.LittleEndian":</span></span>

```qsharp
ApplyWithInputTransformation(LittleEndianAsBigEndian, ApplyXorInPlaceBE, LittleEndian(qubits));
```

## <a name="see-also"></a><span data-ttu-id="ed8bb-119">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ed8bb-119">See Also</span></span>

- [<span data-ttu-id="ed8bb-120">Microsoft. Quantum. Canon. applywithinputtransformation</span><span class="sxs-lookup"><span data-stu-id="ed8bb-120">Microsoft.Quantum.Canon.ApplyWithInputTransformation</span></span>](xref:Microsoft.Quantum.Canon.ApplyWithInputTransformation)
- [<span data-ttu-id="ed8bb-121">Microsoft. Quantum. Canon. applywithinputtransformationa</span><span class="sxs-lookup"><span data-stu-id="ed8bb-121">Microsoft.Quantum.Canon.ApplyWithInputTransformationA</span></span>](xref:Microsoft.Quantum.Canon.ApplyWithInputTransformationA)
- [<span data-ttu-id="ed8bb-122">Microsoft. Quantum. Canon. applywithinputtransformationc</span><span class="sxs-lookup"><span data-stu-id="ed8bb-122">Microsoft.Quantum.Canon.ApplyWithInputTransformationC</span></span>](xref:Microsoft.Quantum.Canon.ApplyWithInputTransformationC)
- [<span data-ttu-id="ed8bb-123">Microsoft. Quantum. Canon. transformedoperation</span><span class="sxs-lookup"><span data-stu-id="ed8bb-123">Microsoft.Quantum.Canon.TransformedOperation</span></span>](xref:Microsoft.Quantum.Canon.TransformedOperation)