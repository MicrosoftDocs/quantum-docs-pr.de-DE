---
uid: Microsoft.Quantum.Optimization.UnivariateOptimizationResult
title: Benutzerdefinierter univariateoptimizationresult-Typ
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Optimization
qsharp.name: UnivariateOptimizationResult
qsharp.summary: Represents the result of optimizing a univariate function.
ms.openlocfilehash: 0bcdbda5586181f965297cb2a398d766f9c6fabb
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96194031"
---
# <a name="univariateoptimizationresult-user-defined-type"></a><span data-ttu-id="b1e86-102">Benutzerdefinierter univariateoptimizationresult-Typ</span><span class="sxs-lookup"><span data-stu-id="b1e86-102">UnivariateOptimizationResult user defined type</span></span>

<span data-ttu-id="b1e86-103">Namespace: [Microsoft. Quantum. Optimization](xref:Microsoft.Quantum.Optimization)</span><span class="sxs-lookup"><span data-stu-id="b1e86-103">Namespace: [Microsoft.Quantum.Optimization](xref:Microsoft.Quantum.Optimization)</span></span>

<span data-ttu-id="b1e86-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="b1e86-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="b1e86-105">Stellt das Ergebnis der Optimierung einer Univariate-Funktion dar.</span><span class="sxs-lookup"><span data-stu-id="b1e86-105">Represents the result of optimizing a univariate function.</span></span>

```qsharp

newtype UnivariateOptimizationResult = (Coordinate : Double, Value : Double);
```



## <a name="named-items"></a><span data-ttu-id="b1e86-106">Benannte Elemente</span><span class="sxs-lookup"><span data-stu-id="b1e86-106">Named Items</span></span>

### <a name="coordinate--double"></a><span data-ttu-id="b1e86-107">Koordinate: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="b1e86-107">Coordinate : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="b1e86-108">Eingabe, bei der eine optimale gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="b1e86-108">Input at which an optimum was found.</span></span>
### <a name="value--double"></a><span data-ttu-id="b1e86-109">Wert: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="b1e86-109">Value : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="b1e86-110">Der Wert, der von der Funktion beim optimalen Wert zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="b1e86-110">Value returned by the function at its optimum.</span></span>