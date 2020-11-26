---
uid: Microsoft.Quantum.AmplitudeAmplification.FixedPointReflectionPhases
title: Fixedpointreflectionphasen-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: FixedPointReflectionPhases
qsharp.summary: Computes partial reflection phases for fixed-point amplitude amplification.
ms.openlocfilehash: 8cc1073447f5fae87ece38db64dcc312f6208899
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96191447"
---
# <a name="fixedpointreflectionphases-function"></a><span data-ttu-id="9ad48-102">Fixedpointreflectionphasen-Funktion</span><span class="sxs-lookup"><span data-stu-id="9ad48-102">FixedPointReflectionPhases function</span></span>

<span data-ttu-id="9ad48-103">Namespace: [Microsoft. Quantum. Verstärkungs Verstärkung](xref:Microsoft.Quantum.AmplitudeAmplification)</span><span class="sxs-lookup"><span data-stu-id="9ad48-103">Namespace: [Microsoft.Quantum.AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span></span>

<span data-ttu-id="9ad48-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="9ad48-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="9ad48-105">Berechnet partielle reflektionsprozesse für die Verstärkung der Amplitude-Amplitude mit fester Breite.</span><span class="sxs-lookup"><span data-stu-id="9ad48-105">Computes partial reflection phases for fixed-point amplitude amplification.</span></span>

```qsharp
function FixedPointReflectionPhases (nQueries : Int, successMin : Double) : Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases
```


## <a name="input"></a><span data-ttu-id="9ad48-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="9ad48-106">Input</span></span>

### <a name="nqueries--int"></a><span data-ttu-id="9ad48-107">nqueries: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="9ad48-107">nQueries : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="9ad48-108">Anzahl von Abfragen für das Zustands Vorbereitungs-Oracle.</span><span class="sxs-lookup"><span data-stu-id="9ad48-108">Number of queries to the state preparation oracle.</span></span> <span data-ttu-id="9ad48-109">Muss eine ungerade ganze Zahl sein.</span><span class="sxs-lookup"><span data-stu-id="9ad48-109">Must be an odd integer.</span></span>


### <a name="successmin--double"></a><span data-ttu-id="9ad48-110">Erfolg: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="9ad48-110">successMin : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="9ad48-111">Die minimale Erfolgswahrscheinlichkeit für das Ziel.</span><span class="sxs-lookup"><span data-stu-id="9ad48-111">Target minimum success probability.</span></span>



## <a name="output--reflectionphases"></a><span data-ttu-id="9ad48-112">Ausgabe: [reflectionphasen](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)</span><span class="sxs-lookup"><span data-stu-id="9ad48-112">Output : [ReflectionPhases](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)</span></span>

<span data-ttu-id="9ad48-113">Ein Array von Phasen, das in der Implementierung eines Quantum-Algorithmus für die fest Komma Verstärkung verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="9ad48-113">Array of phases that can be used in fixed-point amplitude amplification quantum algorithm implementation.</span></span>

## <a name="references"></a><span data-ttu-id="9ad48-114">Referenzen</span><span class="sxs-lookup"><span data-stu-id="9ad48-114">References</span></span>

<span data-ttu-id="9ad48-115">Wir verwenden die Phasen in "Verstärkung mit fester Punkt Amplitude mit einer optimalen Anzahl von Abfragen".</span><span class="sxs-lookup"><span data-stu-id="9ad48-115">We use the phases in "Fixed-Point Amplitude Amplification with an Optimal Number of Queries"</span></span>

- <span data-ttu-id="9ad48-116">[YoderLowChuang2014](https://arxiv.org/abs/1409.3305) Siehe auch "Methodik von zusammengesetzten quantgates"</span><span class="sxs-lookup"><span data-stu-id="9ad48-116">[YoderLowChuang2014](https://arxiv.org/abs/1409.3305) See also "Methodology of composite quantum gates"</span></span>
- <span data-ttu-id="9ad48-117">[LowYoderChuang2016](https://arxiv.org/abs/1603.03996) für Phasen im `RotationPhases` Format.</span><span class="sxs-lookup"><span data-stu-id="9ad48-117">[LowYoderChuang2016](https://arxiv.org/abs/1603.03996) for phases in the `RotationPhases` format.</span></span>