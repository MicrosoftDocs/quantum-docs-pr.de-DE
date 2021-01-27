---
uid: Microsoft.Quantum.Optimization.UnivariateOptimizationResult
title: Benutzerdefinierter univariateoptimizationresult-Typ
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Optimization
qsharp.name: UnivariateOptimizationResult
qsharp.summary: Represents the result of optimizing a univariate function.
ms.openlocfilehash: cc54c0035796aac86482e8a3a6896ceb197c7cfe
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854568"
---
# <a name="univariateoptimizationresult-user-defined-type"></a><span data-ttu-id="af085-102">Benutzerdefinierter univariateoptimizationresult-Typ</span><span class="sxs-lookup"><span data-stu-id="af085-102">UnivariateOptimizationResult user defined type</span></span>

<span data-ttu-id="af085-103">Namespace: [Microsoft. Quantum. Optimization](xref:Microsoft.Quantum.Optimization)</span><span class="sxs-lookup"><span data-stu-id="af085-103">Namespace: [Microsoft.Quantum.Optimization](xref:Microsoft.Quantum.Optimization)</span></span>

<span data-ttu-id="af085-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="af085-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="af085-105">Stellt das Ergebnis der Optimierung einer Univariate-Funktion dar.</span><span class="sxs-lookup"><span data-stu-id="af085-105">Represents the result of optimizing a univariate function.</span></span>

```qsharp

newtype UnivariateOptimizationResult = (Coordinate : Double, Value : Double);
```



## <a name="named-items"></a><span data-ttu-id="af085-106">Benannte Elemente</span><span class="sxs-lookup"><span data-stu-id="af085-106">Named Items</span></span>

### <a name="coordinate--double"></a><span data-ttu-id="af085-107">Koordinate: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="af085-107">Coordinate : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="af085-108">Eingabe, bei der eine optimale gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="af085-108">Input at which an optimum was found.</span></span>
### <a name="value--double"></a><span data-ttu-id="af085-109">Wert: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="af085-109">Value : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="af085-110">Der Wert, der von der Funktion beim optimalen Wert zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="af085-110">Value returned by the function at its optimum.</span></span>