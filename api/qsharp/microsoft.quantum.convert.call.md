---
uid: Microsoft.Quantum.Convert.Call
title: Aufrufvorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: Call
qsharp.summary: Calls a function with a given input.
ms.openlocfilehash: 93458d08aa83ffa8b7b33de8bf51c970af291db9
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850210"
---
# <a name="call-operation"></a><span data-ttu-id="56b42-102">Aufrufvorgang</span><span class="sxs-lookup"><span data-stu-id="56b42-102">Call operation</span></span>

<span data-ttu-id="56b42-103">Namespace: [Microsoft. Quantum. Convert](xref:Microsoft.Quantum.Convert)</span><span class="sxs-lookup"><span data-stu-id="56b42-103">Namespace: [Microsoft.Quantum.Convert](xref:Microsoft.Quantum.Convert)</span></span>

<span data-ttu-id="56b42-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="56b42-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="56b42-105">Ruft eine Funktion mit einer angegebenen Eingabe auf.</span><span class="sxs-lookup"><span data-stu-id="56b42-105">Calls a function with a given input.</span></span>

```qsharp
operation Call<'Input, 'Output> (fn : ('Input -> 'Output), input : 'Input) : 'Output
```


## <a name="description"></a><span data-ttu-id="56b42-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="56b42-106">Description</span></span>

<span data-ttu-id="56b42-107">Wenn eine Funktion und eine Eingabe für diese Funktion angegeben sind, ruft die Funktion auf und gibt Ihre Ausgabe zurück.</span><span class="sxs-lookup"><span data-stu-id="56b42-107">Given a function and an input to that function, calls the function and returns its output.</span></span>

## <a name="input"></a><span data-ttu-id="56b42-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="56b42-108">Input</span></span>

### <a name="fn--input---output"></a><span data-ttu-id="56b42-109">FN: "Input->"-Ausgabe</span><span class="sxs-lookup"><span data-stu-id="56b42-109">fn : 'Input -> 'Output</span></span>

<span data-ttu-id="56b42-110">Eine Funktion, die aufgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="56b42-110">A function to be called.</span></span>


### <a name="input--input"></a><span data-ttu-id="56b42-111">Eingabe: ' Eingabe</span><span class="sxs-lookup"><span data-stu-id="56b42-111">input : 'Input</span></span>

<span data-ttu-id="56b42-112">Die Eingabe, die an die Funktion übermittelt werden soll.</span><span class="sxs-lookup"><span data-stu-id="56b42-112">The input to be passed to the function.</span></span>



## <a name="output--output"></a><span data-ttu-id="56b42-113">Ausgabe: "Output</span><span class="sxs-lookup"><span data-stu-id="56b42-113">Output : 'Output</span></span>

<span data-ttu-id="56b42-114">Das Ergebnis des Aufrufs von `fn`.</span><span class="sxs-lookup"><span data-stu-id="56b42-114">The result of calling `fn`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="56b42-115">Typparameter</span><span class="sxs-lookup"><span data-stu-id="56b42-115">Type Parameters</span></span>

### <a name="input"></a><span data-ttu-id="56b42-116">' Eingabe</span><span class="sxs-lookup"><span data-stu-id="56b42-116">'Input</span></span>


### <a name="output"></a><span data-ttu-id="56b42-117">' Ausgabe</span><span class="sxs-lookup"><span data-stu-id="56b42-117">'Output</span></span>



## <a name="remarks"></a><span data-ttu-id="56b42-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="56b42-118">Remarks</span></span>

<span data-ttu-id="56b42-119">Dieser Vorgang ist besonders nützlich, um zu erzwingen, dass eine Funktion an einer bestimmten Stelle innerhalb eines Vorgangs aufgerufen wird, oder zum Aufrufen einer Funktion, bei der ein Vorgang erwartet wird.</span><span class="sxs-lookup"><span data-stu-id="56b42-119">This operation is mainly useful for forcing a function to be called at a specific place within an operation, or for calling a function where an operation is expected.</span></span>