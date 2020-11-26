---
uid: Microsoft.Quantum.Optimization.LocalUnivariateMinimum
title: Localunivariateminimum-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Optimization
qsharp.name: LocalUnivariateMinimum
qsharp.summary: Returns the local minimum for a univariate function over a bounded interval, using a golden interval search.
ms.openlocfilehash: e804e6a6ed82f14dcc9b8f721ad503d77922dc0f
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96194082"
---
# <a name="localunivariateminimum-function"></a><span data-ttu-id="454ae-102">Localunivariateminimum-Funktion</span><span class="sxs-lookup"><span data-stu-id="454ae-102">LocalUnivariateMinimum function</span></span>

<span data-ttu-id="454ae-103">Namespace: [Microsoft. Quantum. Optimization](xref:Microsoft.Quantum.Optimization)</span><span class="sxs-lookup"><span data-stu-id="454ae-103">Namespace: [Microsoft.Quantum.Optimization](xref:Microsoft.Quantum.Optimization)</span></span>

<span data-ttu-id="454ae-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="454ae-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="454ae-105">Gibt das lokale Minimum für eine Univariate-Funktion über ein begrenztes Intervall zurück, wobei eine Golden Interval-Suche verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="454ae-105">Returns the local minimum for a univariate function over a bounded interval, using a golden interval search.</span></span>

```qsharp
function LocalUnivariateMinimum (fn : (Double -> Double), bounds : (Double, Double), tolerance : Double) : Microsoft.Quantum.Optimization.UnivariateOptimizationResult
```


## <a name="input"></a><span data-ttu-id="454ae-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="454ae-106">Input</span></span>

### <a name="fn--double---double"></a><span data-ttu-id="454ae-107">FN: [Double](xref:microsoft.quantum.lang-ref.double) -> [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="454ae-107">fn : [Double](xref:microsoft.quantum.lang-ref.double) -> [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="454ae-108">Die Univariate-Funktion, die minimiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="454ae-108">The univariate function to be minimized.</span></span>


### <a name="bounds--doubledouble"></a><span data-ttu-id="454ae-109">Begrenzungen: ([Double](xref:microsoft.quantum.lang-ref.double),[Double](xref:microsoft.quantum.lang-ref.double))</span><span class="sxs-lookup"><span data-stu-id="454ae-109">bounds : ([Double](xref:microsoft.quantum.lang-ref.double),[Double](xref:microsoft.quantum.lang-ref.double))</span></span>

<span data-ttu-id="454ae-110">Das Intervall, in dem das lokale Minimum zu finden ist.</span><span class="sxs-lookup"><span data-stu-id="454ae-110">The interval in which the local minimum is to be found.</span></span>


### <a name="tolerance--double"></a><span data-ttu-id="454ae-111">Toleranz: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="454ae-111">tolerance : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="454ae-112">Die Genauigkeit in der zu tolerier enden Funktions Eingabe.</span><span class="sxs-lookup"><span data-stu-id="454ae-112">The accuracy in the function input to be tolerated.</span></span>
<span data-ttu-id="454ae-113">Die Suche nach lokalem Optima wird fortgesetzt, bis das Intervall kleiner als diese Toleranz ist.</span><span class="sxs-lookup"><span data-stu-id="454ae-113">The search for local optima will continue until the interval is smaller in width than this tolerance.</span></span>



## <a name="output--univariateoptimizationresult"></a><span data-ttu-id="454ae-114">Ausgabe: [univariateoptimizationresult](xref:Microsoft.Quantum.Optimization.UnivariateOptimizationResult)</span><span class="sxs-lookup"><span data-stu-id="454ae-114">Output : [UnivariateOptimizationResult](xref:Microsoft.Quantum.Optimization.UnivariateOptimizationResult)</span></span>

<span data-ttu-id="454ae-115">Ein lokaler Optima der angegebenen Funktion, der sich innerhalb der angegebenen Begrenzungen befindet.</span><span class="sxs-lookup"><span data-stu-id="454ae-115">A local optima of the given function, located within the given bounds.</span></span>