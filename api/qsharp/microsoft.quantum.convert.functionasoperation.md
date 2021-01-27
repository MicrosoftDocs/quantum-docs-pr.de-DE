---
uid: Microsoft.Quantum.Convert.FunctionAsOperation
title: Functionasoperation-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: FunctionAsOperation
qsharp.summary: Converts functions to operations.
ms.openlocfilehash: cf4f8c97bf38b3a64eb952d0a502bc21c29c579c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98833838"
---
# <a name="functionasoperation-function"></a><span data-ttu-id="101d0-102">Functionasoperation-Funktion</span><span class="sxs-lookup"><span data-stu-id="101d0-102">FunctionAsOperation function</span></span>

<span data-ttu-id="101d0-103">Namespace: [Microsoft. Quantum. Convert](xref:Microsoft.Quantum.Convert)</span><span class="sxs-lookup"><span data-stu-id="101d0-103">Namespace: [Microsoft.Quantum.Convert](xref:Microsoft.Quantum.Convert)</span></span>

<span data-ttu-id="101d0-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="101d0-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="101d0-105">Konvertiert Funktionen in Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="101d0-105">Converts functions to operations.</span></span>

```qsharp
function FunctionAsOperation<'Input, 'Output> (fn : ('Input -> 'Output)) : ('Input => 'Output)
```


## <a name="description"></a><span data-ttu-id="101d0-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="101d0-106">Description</span></span>

<span data-ttu-id="101d0-107">Gibt bei Angabe einer Funktion einen Vorgang zurück, der diese Funktion aufruft, und der nichts anderes bewirkt.</span><span class="sxs-lookup"><span data-stu-id="101d0-107">Given a function, returns an operation which calls that function, and which does nothing else.</span></span>

## <a name="input"></a><span data-ttu-id="101d0-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="101d0-108">Input</span></span>

### <a name="fn--input---output"></a><span data-ttu-id="101d0-109">FN: "Input->"-Ausgabe</span><span class="sxs-lookup"><span data-stu-id="101d0-109">fn : 'Input -> 'Output</span></span>

<span data-ttu-id="101d0-110">Eine Funktion, die in einen Vorgang konvertiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="101d0-110">A function to be converted to an operation.</span></span>



## <a name="output--input--output"></a><span data-ttu-id="101d0-111">Ausgabe: Eingabe => Ausgabe</span><span class="sxs-lookup"><span data-stu-id="101d0-111">Output : 'Input => 'Output</span></span> 

<span data-ttu-id="101d0-112">Ein Vorgang `op` , der `op(input)` mit `fn(input)` for all identisch ist `input` .</span><span class="sxs-lookup"><span data-stu-id="101d0-112">An operation `op` such that `op(input)` is identical to `fn(input)` for all `input`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="101d0-113">Typparameter</span><span class="sxs-lookup"><span data-stu-id="101d0-113">Type Parameters</span></span>

### <a name="input"></a><span data-ttu-id="101d0-114">' Eingabe</span><span class="sxs-lookup"><span data-stu-id="101d0-114">'Input</span></span>

<span data-ttu-id="101d0-115">Der Eingabetyp der Funktion, die konvertiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="101d0-115">Input type of the function to be converted.</span></span>
### <a name="output"></a><span data-ttu-id="101d0-116">' Ausgabe</span><span class="sxs-lookup"><span data-stu-id="101d0-116">'Output</span></span>

<span data-ttu-id="101d0-117">Der Ausgabetyp der Funktion, die konvertiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="101d0-117">Output type of the function to be converted.</span></span>

## <a name="remarks"></a><span data-ttu-id="101d0-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="101d0-118">Remarks</span></span>

<span data-ttu-id="101d0-119">Dies ist vor allem nützlich für das Übergeben von Funktionen an Funktionen oder Vorgänge, die einen Vorgang als Eingabe erwarten.</span><span class="sxs-lookup"><span data-stu-id="101d0-119">This is mainly useful for passing functions to functions or operations which expect an operation as input.</span></span>