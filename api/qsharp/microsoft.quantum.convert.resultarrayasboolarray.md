---
uid: Microsoft.Quantum.Convert.ResultArrayAsBoolArray
title: Resultarrayasboolarray-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: ResultArrayAsBoolArray
qsharp.summary: Converts a `Result[]` type to a `Bool[]` type, where `One` is mapped to `true` and `Zero` is mapped to `false`.
ms.openlocfilehash: 0356fe9c98306ee3e1857f4af311aef9b3789a7d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702918"
---
# <a name="resultarrayasboolarray-function"></a><span data-ttu-id="e7602-102">Resultarrayasboolarray-Funktion</span><span class="sxs-lookup"><span data-stu-id="e7602-102">ResultArrayAsBoolArray function</span></span>

<span data-ttu-id="e7602-103">Namespace: [Microsoft. Quantum. Convert](xref:Microsoft.Quantum.Convert)</span><span class="sxs-lookup"><span data-stu-id="e7602-103">Namespace: [Microsoft.Quantum.Convert](xref:Microsoft.Quantum.Convert)</span></span>

<span data-ttu-id="e7602-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="e7602-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="e7602-105">Konvertiert einen `Result[]` Typ in einen `Bool[]` -Typ, wobei `One` zugeordnet ist `true` und `Zero` zugeordnet ist `false` .</span><span class="sxs-lookup"><span data-stu-id="e7602-105">Converts a `Result[]` type to a `Bool[]` type, where `One` is mapped to `true` and `Zero` is mapped to `false`.</span></span>

```qsharp
function ResultArrayAsBoolArray (input : Result[]) : Bool[]
```


## <a name="input"></a><span data-ttu-id="e7602-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e7602-106">Input</span></span>

### <a name="input--__invalidresult__"></a><span data-ttu-id="e7602-107">Eingabe: __ungültig <Result>__ []</span><span class="sxs-lookup"><span data-stu-id="e7602-107">input : __invalid<Result>__ []</span></span>

<span data-ttu-id="e7602-108">`Result[]` , das konvertiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="e7602-108">`Result[]` to be converted.</span></span>



## <a name="output--bool"></a><span data-ttu-id="e7602-109">Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)[]</span><span class="sxs-lookup"><span data-stu-id="e7602-109">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span></span>

<span data-ttu-id="e7602-110">Die `Bool[]`, die das `input` darstellt.</span><span class="sxs-lookup"><span data-stu-id="e7602-110">A `Bool[]` representing the `input`.</span></span>