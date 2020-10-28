---
uid: Microsoft.Quantum.Convert.Call
title: Aufrufvorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: Call
qsharp.summary: Calls a function with a given input.
ms.openlocfilehash: 8630f846b4b9823ce1c1dfd61dc8ca81e468517d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702995"
---
# <a name="call-operation"></a><span data-ttu-id="d73c2-102">Aufrufvorgang</span><span class="sxs-lookup"><span data-stu-id="d73c2-102">Call operation</span></span>

<span data-ttu-id="d73c2-103">Namespace: [Microsoft. Quantum. Convert](xref:Microsoft.Quantum.Convert)</span><span class="sxs-lookup"><span data-stu-id="d73c2-103">Namespace: [Microsoft.Quantum.Convert](xref:Microsoft.Quantum.Convert)</span></span>

<span data-ttu-id="d73c2-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="d73c2-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="d73c2-105">Ruft eine Funktion mit einer angegebenen Eingabe auf.</span><span class="sxs-lookup"><span data-stu-id="d73c2-105">Calls a function with a given input.</span></span>

```qsharp
operation Call<'Input, 'Output> (fn : ('Input -> 'Output), input : 'Input) : 'Output
```


## <a name="description"></a><span data-ttu-id="d73c2-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d73c2-106">Description</span></span>

<span data-ttu-id="d73c2-107">Wenn eine Funktion und eine Eingabe für diese Funktion angegeben sind, ruft die Funktion auf und gibt Ihre Ausgabe zurück.</span><span class="sxs-lookup"><span data-stu-id="d73c2-107">Given a function and an input to that function, calls the function and returns its output.</span></span>

## <a name="input"></a><span data-ttu-id="d73c2-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d73c2-108">Input</span></span>

### <a name="fn--input---output"></a><span data-ttu-id="d73c2-109">FN: "Input->"-Ausgabe</span><span class="sxs-lookup"><span data-stu-id="d73c2-109">fn : 'Input -> 'Output</span></span>

<span data-ttu-id="d73c2-110">Eine Funktion, die aufgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="d73c2-110">A function to be called.</span></span>


### <a name="input--input"></a><span data-ttu-id="d73c2-111">Eingabe: ' Eingabe</span><span class="sxs-lookup"><span data-stu-id="d73c2-111">input : 'Input</span></span>

<span data-ttu-id="d73c2-112">Die Eingabe, die an die Funktion übermittelt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d73c2-112">The input to be passed to the function.</span></span>



## <a name="output--output"></a><span data-ttu-id="d73c2-113">Ausgabe: "Output</span><span class="sxs-lookup"><span data-stu-id="d73c2-113">Output : 'Output</span></span>

<span data-ttu-id="d73c2-114">Das Ergebnis des Aufrufs von `fn`.</span><span class="sxs-lookup"><span data-stu-id="d73c2-114">The result of calling `fn`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="d73c2-115">Typparameter</span><span class="sxs-lookup"><span data-stu-id="d73c2-115">Type Parameters</span></span>

### <a name="input"></a><span data-ttu-id="d73c2-116">' Eingabe</span><span class="sxs-lookup"><span data-stu-id="d73c2-116">'Input</span></span>


### <a name="output"></a><span data-ttu-id="d73c2-117">' Ausgabe</span><span class="sxs-lookup"><span data-stu-id="d73c2-117">'Output</span></span>



## <a name="remarks"></a><span data-ttu-id="d73c2-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d73c2-118">Remarks</span></span>

<span data-ttu-id="d73c2-119">Dieser Vorgang ist besonders nützlich, um zu erzwingen, dass eine Funktion an einer bestimmten Stelle innerhalb eines Vorgangs aufgerufen wird, oder zum Aufrufen einer Funktion, bei der ein Vorgang erwartet wird.</span><span class="sxs-lookup"><span data-stu-id="d73c2-119">This operation is mainly useful for forcing a function to be called at a specific place within an operation, or for calling a function where an operation is expected.</span></span>