---
uid: Microsoft.Quantum.Optimization.UnivariateOptimizationResult
title: Benutzerdefinierter univariateoptimizationresult-Typ
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Optimization
qsharp.name: UnivariateOptimizationResult
qsharp.summary: Represents the result of optimizing a univariate function.
ms.openlocfilehash: c8aa91bbdc9e9e9bb4d110b470ff2041f9460a38
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92724320"
---
# <a name="univariateoptimizationresult-user-defined-type"></a><span data-ttu-id="cfcbc-102">Benutzerdefinierter univariateoptimizationresult-Typ</span><span class="sxs-lookup"><span data-stu-id="cfcbc-102">UnivariateOptimizationResult user defined type</span></span>

<span data-ttu-id="cfcbc-103">Namespace: [Microsoft. Quantum. Optimization](xref:Microsoft.Quantum.Optimization)</span><span class="sxs-lookup"><span data-stu-id="cfcbc-103">Namespace: [Microsoft.Quantum.Optimization](xref:Microsoft.Quantum.Optimization)</span></span>

<span data-ttu-id="cfcbc-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="cfcbc-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="cfcbc-105">Stellt das Ergebnis der Optimierung einer Univariate-Funktion dar.</span><span class="sxs-lookup"><span data-stu-id="cfcbc-105">Represents the result of optimizing a univariate function.</span></span>

```qsharp

newtype UnivariateOptimizationResult = (Coordinate : Double, Value : Double);
```



## <a name="named-items"></a><span data-ttu-id="cfcbc-106">Benannte Elemente</span><span class="sxs-lookup"><span data-stu-id="cfcbc-106">Named Items</span></span>

### <a name="coordinate--double"></a><span data-ttu-id="cfcbc-107">Koordinate: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="cfcbc-107">Coordinate : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="cfcbc-108">Eingabe, bei der eine optimale gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="cfcbc-108">Input at which an optimum was found.</span></span>
### <a name="value--double"></a><span data-ttu-id="cfcbc-109">Wert: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="cfcbc-109">Value : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="cfcbc-110">Der Wert, der von der Funktion beim optimalen Wert zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="cfcbc-110">Value returned by the function at its optimum.</span></span>