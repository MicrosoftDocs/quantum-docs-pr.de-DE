---
uid: Microsoft.Quantum.Convert.FunctionAsOperation
title: Functionasoperation-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: FunctionAsOperation
qsharp.summary: Converts functions to operations.
ms.openlocfilehash: 90e9f0c922a77fbb6d6faf8945d4f5d1c8ff33b7
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702984"
---
# <a name="functionasoperation-function"></a><span data-ttu-id="16216-102">Functionasoperation-Funktion</span><span class="sxs-lookup"><span data-stu-id="16216-102">FunctionAsOperation function</span></span>

<span data-ttu-id="16216-103">Namespace: [Microsoft. Quantum. Convert](xref:Microsoft.Quantum.Convert)</span><span class="sxs-lookup"><span data-stu-id="16216-103">Namespace: [Microsoft.Quantum.Convert](xref:Microsoft.Quantum.Convert)</span></span>

<span data-ttu-id="16216-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="16216-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="16216-105">Konvertiert Funktionen in Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="16216-105">Converts functions to operations.</span></span>

```qsharp
function FunctionAsOperation<'Input, 'Output> (fn : ('Input -> 'Output)) : ('Input => 'Output)
```


## <a name="description"></a><span data-ttu-id="16216-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="16216-106">Description</span></span>

<span data-ttu-id="16216-107">Gibt bei Angabe einer Funktion einen Vorgang zurück, der diese Funktion aufruft, und der nichts anderes bewirkt.</span><span class="sxs-lookup"><span data-stu-id="16216-107">Given a function, returns an operation which calls that function, and which does nothing else.</span></span>

## <a name="input"></a><span data-ttu-id="16216-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="16216-108">Input</span></span>

### <a name="fn--input---output"></a><span data-ttu-id="16216-109">FN: "Input->"-Ausgabe</span><span class="sxs-lookup"><span data-stu-id="16216-109">fn : 'Input -> 'Output</span></span>

<span data-ttu-id="16216-110">Eine Funktion, die in einen Vorgang konvertiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="16216-110">A function to be converted to an operation.</span></span>



## <a name="output--input--output"></a><span data-ttu-id="16216-111">Ausgabe: Eingabe => Ausgabe</span><span class="sxs-lookup"><span data-stu-id="16216-111">Output : 'Input => 'Output</span></span> 

<span data-ttu-id="16216-112">Ein Vorgang `op` , der `op(input)` mit `fn(input)` for all identisch ist `input` .</span><span class="sxs-lookup"><span data-stu-id="16216-112">An operation `op` such that `op(input)` is identical to `fn(input)` for all `input`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="16216-113">Typparameter</span><span class="sxs-lookup"><span data-stu-id="16216-113">Type Parameters</span></span>

### <a name="input"></a><span data-ttu-id="16216-114">' Eingabe</span><span class="sxs-lookup"><span data-stu-id="16216-114">'Input</span></span>

<span data-ttu-id="16216-115">Der Eingabetyp der Funktion, die konvertiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="16216-115">Input type of the function to be converted.</span></span>
### <a name="output"></a><span data-ttu-id="16216-116">' Ausgabe</span><span class="sxs-lookup"><span data-stu-id="16216-116">'Output</span></span>

<span data-ttu-id="16216-117">Der Ausgabetyp der Funktion, die konvertiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="16216-117">Output type of the function to be converted.</span></span>

## <a name="remarks"></a><span data-ttu-id="16216-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="16216-118">Remarks</span></span>

<span data-ttu-id="16216-119">Dies ist vor allem nützlich für das Übergeben von Funktionen an Funktionen oder Vorgänge, die einen Vorgang als Eingabe erwarten.</span><span class="sxs-lookup"><span data-stu-id="16216-119">This is mainly useful for passing functions to functions or operations which expect an operation as input.</span></span>