---
uid: Microsoft.Quantum.Convert.BoolArrayAsResultArray
title: Boolarrayasresultarray-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: BoolArrayAsResultArray
qsharp.summary: Converts a `Bool[]` type to a `Result[]` type, where `true` is mapped to `One` and `false` is mapped to `Zero`.
ms.openlocfilehash: b30da07272ee1a6c19ae13afa618ba5deb7aaa2d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98834192"
---
# <a name="boolarrayasresultarray-function"></a><span data-ttu-id="d1107-102">Boolarrayasresultarray-Funktion</span><span class="sxs-lookup"><span data-stu-id="d1107-102">BoolArrayAsResultArray function</span></span>

<span data-ttu-id="d1107-103">Namespace: [Microsoft. Quantum. Convert](xref:Microsoft.Quantum.Convert)</span><span class="sxs-lookup"><span data-stu-id="d1107-103">Namespace: [Microsoft.Quantum.Convert](xref:Microsoft.Quantum.Convert)</span></span>

<span data-ttu-id="d1107-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="d1107-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="d1107-105">Konvertiert einen `Bool[]` Typ in einen `Result[]` -Typ, wobei `true` zugeordnet ist `One` und `false` zugeordnet ist `Zero` .</span><span class="sxs-lookup"><span data-stu-id="d1107-105">Converts a `Bool[]` type to a `Result[]` type, where `true` is mapped to `One` and `false` is mapped to `Zero`.</span></span>

```qsharp
function BoolArrayAsResultArray (input : Bool[]) : Result[]
```


## <a name="input"></a><span data-ttu-id="d1107-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d1107-106">Input</span></span>

### <a name="input--bool"></a><span data-ttu-id="d1107-107">Eingabe: [bool](xref:microsoft.quantum.lang-ref.bool)[]</span><span class="sxs-lookup"><span data-stu-id="d1107-107">input : [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span></span>

<span data-ttu-id="d1107-108">`Bool[]` , das konvertiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="d1107-108">`Bool[]` to be converted.</span></span>



## <a name="output--__invalidresult__"></a><span data-ttu-id="d1107-109">Ausgabe: __ungültig <Result>__[]</span><span class="sxs-lookup"><span data-stu-id="d1107-109">Output : __invalid<Result>__[]</span></span>

<span data-ttu-id="d1107-110">Die `Result[]`, die das `input` darstellt.</span><span class="sxs-lookup"><span data-stu-id="d1107-110">A `Result[]` representing the `input`.</span></span>