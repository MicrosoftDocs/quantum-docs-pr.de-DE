---
uid: Microsoft.Quantum.Random.StandardNormalDistribution
title: Standardnormaldistribution-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: StandardNormalDistribution
qsharp.summary: Returns a normal distribution with mean 0 and variance 1.
ms.openlocfilehash: e1776339655c33516f7b3d156f1b377a0c74d250
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98857798"
---
# <a name="standardnormaldistribution-function"></a><span data-ttu-id="848d9-102">Standardnormaldistribution-Funktion</span><span class="sxs-lookup"><span data-stu-id="848d9-102">StandardNormalDistribution function</span></span>

<span data-ttu-id="848d9-103">Namespace: [Microsoft. Quantum. Random](xref:Microsoft.Quantum.Random)</span><span class="sxs-lookup"><span data-stu-id="848d9-103">Namespace: [Microsoft.Quantum.Random](xref:Microsoft.Quantum.Random)</span></span>

<span data-ttu-id="848d9-104">Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="848d9-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="848d9-105">Gibt eine normale Verteilung mit dem Mittelwert 0 und der Varianz 1 zurück.</span><span class="sxs-lookup"><span data-stu-id="848d9-105">Returns a normal distribution with mean 0 and variance 1.</span></span>

```qsharp
function StandardNormalDistribution () : Microsoft.Quantum.Random.ContinuousDistribution
```


## <a name="output--continuousdistribution"></a><span data-ttu-id="848d9-106">Ausgabe: [continuousdistribution](xref:Microsoft.Quantum.Random.ContinuousDistribution)</span><span class="sxs-lookup"><span data-stu-id="848d9-106">Output : [ContinuousDistribution](xref:Microsoft.Quantum.Random.ContinuousDistribution)</span></span>



## <a name="example"></a><span data-ttu-id="848d9-107">Beispiel</span><span class="sxs-lookup"><span data-stu-id="848d9-107">Example</span></span>

<span data-ttu-id="848d9-108">Der folgende Code zeichnet 10 Beispiele aus der standardmäßigen Normalverteilung:</span><span class="sxs-lookup"><span data-stu-id="848d9-108">The following draws 10 samples from the standard normal distribution:</span></span>

```qsharp
let samples = DrawMany((StandardNormalDistribution())::Sample, 10, ());
```

## <a name="see-also"></a><span data-ttu-id="848d9-109">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="848d9-109">See Also</span></span>

- [<span data-ttu-id="848d9-110">Microsoft. Quantum. Random. normaldistribution</span><span class="sxs-lookup"><span data-stu-id="848d9-110">Microsoft.Quantum.Random.NormalDistribution</span></span>](xref:Microsoft.Quantum.Random.NormalDistribution)