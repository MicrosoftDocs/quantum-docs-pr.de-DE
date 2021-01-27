---
uid: Microsoft.Quantum.Random.NormalDistribution
title: Normaldistribution-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: NormalDistribution
qsharp.summary: Returns a normal distribution with a given mean and variance.
ms.openlocfilehash: 733a2763dca6d75f81d538f63c3084331a8e1d51
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98814182"
---
# <a name="normaldistribution-function"></a><span data-ttu-id="30ca5-102">Normaldistribution-Funktion</span><span class="sxs-lookup"><span data-stu-id="30ca5-102">NormalDistribution function</span></span>

<span data-ttu-id="30ca5-103">Namespace: [Microsoft. Quantum. Random](xref:Microsoft.Quantum.Random)</span><span class="sxs-lookup"><span data-stu-id="30ca5-103">Namespace: [Microsoft.Quantum.Random](xref:Microsoft.Quantum.Random)</span></span>

<span data-ttu-id="30ca5-104">Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="30ca5-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="30ca5-105">Gibt eine normale Verteilung mit einem angegebenen Mittelwert und Varianz zurück.</span><span class="sxs-lookup"><span data-stu-id="30ca5-105">Returns a normal distribution with a given mean and variance.</span></span>

```qsharp
function NormalDistribution (mean : Double, variance : Double) : Microsoft.Quantum.Random.ContinuousDistribution
```


## <a name="input"></a><span data-ttu-id="30ca5-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="30ca5-106">Input</span></span>

### <a name="mean--double"></a><span data-ttu-id="30ca5-107">Mittelwert: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="30ca5-107">mean : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>




### <a name="variance--double"></a><span data-ttu-id="30ca5-108">Varianz: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="30ca5-108">variance : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>





## <a name="output--continuousdistribution"></a><span data-ttu-id="30ca5-109">Ausgabe: [continuousdistribution](xref:Microsoft.Quantum.Random.ContinuousDistribution)</span><span class="sxs-lookup"><span data-stu-id="30ca5-109">Output : [ContinuousDistribution](xref:Microsoft.Quantum.Random.ContinuousDistribution)</span></span>



## <a name="example"></a><span data-ttu-id="30ca5-110">Beispiel</span><span class="sxs-lookup"><span data-stu-id="30ca5-110">Example</span></span>

<span data-ttu-id="30ca5-111">Der folgende Code zeichnet 10 Beispiele aus der normalen Verteilung mit dem Mittelwert 2 und der Standardabweichung 0,1:</span><span class="sxs-lookup"><span data-stu-id="30ca5-111">The following draws 10 samples from the normal distribution with mean 2 and standard deviation 0.1:</span></span>

```qsharp
let samples = DrawMany(
    (NormalDistribution(2.0, PowD(0.1, 2.0)))::Sample,
    10, ()
);
```

## <a name="see-also"></a><span data-ttu-id="30ca5-112">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="30ca5-112">See Also</span></span>

- [<span data-ttu-id="30ca5-113">Microsoft. Quantum. Random. standardnormaldistribution</span><span class="sxs-lookup"><span data-stu-id="30ca5-113">Microsoft.Quantum.Random.StandardNormalDistribution</span></span>](xref:Microsoft.Quantum.Random.StandardNormalDistribution)