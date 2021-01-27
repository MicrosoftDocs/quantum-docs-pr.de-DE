---
uid: Microsoft.Quantum.AmplitudeAmplification.FixedPointReflectionPhases
title: Fixedpointreflectionphasen-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: FixedPointReflectionPhases
qsharp.summary: Computes partial reflection phases for fixed-point amplitude amplification.
ms.openlocfilehash: 2ded197801111c26d8a33f9c2363b46ca4b6c4b9
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845854"
---
# <a name="fixedpointreflectionphases-function"></a><span data-ttu-id="23d79-102">Fixedpointreflectionphasen-Funktion</span><span class="sxs-lookup"><span data-stu-id="23d79-102">FixedPointReflectionPhases function</span></span>

<span data-ttu-id="23d79-103">Namespace: [Microsoft. Quantum. Verstärkungs Verstärkung](xref:Microsoft.Quantum.AmplitudeAmplification)</span><span class="sxs-lookup"><span data-stu-id="23d79-103">Namespace: [Microsoft.Quantum.AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span></span>

<span data-ttu-id="23d79-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="23d79-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="23d79-105">Berechnet partielle reflektionsprozesse für die Verstärkung der Amplitude-Amplitude mit fester Breite.</span><span class="sxs-lookup"><span data-stu-id="23d79-105">Computes partial reflection phases for fixed-point amplitude amplification.</span></span>

```qsharp
function FixedPointReflectionPhases (nQueries : Int, successMin : Double) : Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases
```


## <a name="input"></a><span data-ttu-id="23d79-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="23d79-106">Input</span></span>

### <a name="nqueries--int"></a><span data-ttu-id="23d79-107">nqueries: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="23d79-107">nQueries : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="23d79-108">Anzahl von Abfragen für das Zustands Vorbereitungs-Oracle.</span><span class="sxs-lookup"><span data-stu-id="23d79-108">Number of queries to the state preparation oracle.</span></span> <span data-ttu-id="23d79-109">Muss eine ungerade ganze Zahl sein.</span><span class="sxs-lookup"><span data-stu-id="23d79-109">Must be an odd integer.</span></span>


### <a name="successmin--double"></a><span data-ttu-id="23d79-110">Erfolg: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="23d79-110">successMin : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="23d79-111">Die minimale Erfolgswahrscheinlichkeit für das Ziel.</span><span class="sxs-lookup"><span data-stu-id="23d79-111">Target minimum success probability.</span></span>



## <a name="output--reflectionphases"></a><span data-ttu-id="23d79-112">Ausgabe: [reflectionphasen](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)</span><span class="sxs-lookup"><span data-stu-id="23d79-112">Output : [ReflectionPhases](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)</span></span>

<span data-ttu-id="23d79-113">Ein Array von Phasen, das in der Implementierung eines Quantum-Algorithmus für die fest Komma Verstärkung verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="23d79-113">Array of phases that can be used in fixed-point amplitude amplification quantum algorithm implementation.</span></span>

## <a name="references"></a><span data-ttu-id="23d79-114">References</span><span class="sxs-lookup"><span data-stu-id="23d79-114">References</span></span>

<span data-ttu-id="23d79-115">Wir verwenden die Phasen in "Verstärkung mit fester Punkt Amplitude mit einer optimalen Anzahl von Abfragen".</span><span class="sxs-lookup"><span data-stu-id="23d79-115">We use the phases in "Fixed-Point Amplitude Amplification with an Optimal Number of Queries"</span></span>

- <span data-ttu-id="23d79-116">[YoderLowChuang2014](https://arxiv.org/abs/1409.3305) Siehe auch "Methodik von zusammengesetzten quantgates"</span><span class="sxs-lookup"><span data-stu-id="23d79-116">[YoderLowChuang2014](https://arxiv.org/abs/1409.3305) See also "Methodology of composite quantum gates"</span></span>
- <span data-ttu-id="23d79-117">[LowYoderChuang2016](https://arxiv.org/abs/1603.03996) für Phasen im `RotationPhases` Format.</span><span class="sxs-lookup"><span data-stu-id="23d79-117">[LowYoderChuang2016](https://arxiv.org/abs/1603.03996) for phases in the `RotationPhases` format.</span></span>