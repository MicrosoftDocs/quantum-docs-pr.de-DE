---
uid: Microsoft.Quantum.AmplitudeAmplification.AmplitudeAmplificationFromStatePreparation
title: Verstärkungsfromstatepreparation-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: AmplitudeAmplificationFromStatePreparation
qsharp.summary: Amplitude amplification by oracles for partial reflections.
ms.openlocfilehash: 30e1cf6e353b8a4491e13a9e2f588ec9cc103cb4
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96191600"
---
# <a name="amplitudeamplificationfromstatepreparation-function"></a><span data-ttu-id="abf8b-102">Verstärkungsfromstatepreparation-Funktion</span><span class="sxs-lookup"><span data-stu-id="abf8b-102">AmplitudeAmplificationFromStatePreparation function</span></span>

<span data-ttu-id="abf8b-103">Namespace: [Microsoft. Quantum. Verstärkungs Verstärkung](xref:Microsoft.Quantum.AmplitudeAmplification)</span><span class="sxs-lookup"><span data-stu-id="abf8b-103">Namespace: [Microsoft.Quantum.AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span></span>

<span data-ttu-id="abf8b-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="abf8b-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="abf8b-105">Amplitude-Verstärkung durch Oracles für partielle Reflektionen.</span><span class="sxs-lookup"><span data-stu-id="abf8b-105">Amplitude amplification by oracles for partial reflections.</span></span>

```qsharp
function AmplitudeAmplificationFromStatePreparation (phases : Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases, stateOracle : Microsoft.Quantum.Oracles.StateOracle, idxFlagQubit : Int) : (Qubit[] => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="abf8b-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="abf8b-106">Input</span></span>

### <a name="phases--reflectionphases"></a><span data-ttu-id="abf8b-107">Phasen: [reflectionphasen](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)</span><span class="sxs-lookup"><span data-stu-id="abf8b-107">phases : [ReflectionPhases](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)</span></span>

<span data-ttu-id="abf8b-108">Phasen von partiellen Reflektionen</span><span class="sxs-lookup"><span data-stu-id="abf8b-108">Phases of partial reflections</span></span>


### <a name="stateoracle--stateoracle"></a><span data-ttu-id="abf8b-109">stateoracle: [stateoracle](xref:Microsoft.Quantum.Oracles.StateOracle)</span><span class="sxs-lookup"><span data-stu-id="abf8b-109">stateOracle : [StateOracle](xref:Microsoft.Quantum.Oracles.StateOracle)</span></span>

<span data-ttu-id="abf8b-110">Einheitlicher Oracle-$A $, der den Startstatus vorbereitet</span><span class="sxs-lookup"><span data-stu-id="abf8b-110">Unitary oracle $A$ that prepares start state</span></span>


### <a name="idxflagqubit--int"></a><span data-ttu-id="abf8b-111">idxflagqubit: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="abf8b-111">idxFlagQubit : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="abf8b-112">Index zum Markieren von Qubit</span><span class="sxs-lookup"><span data-stu-id="abf8b-112">Index to flag qubit</span></span>



## <a name="output--qubit--unit--is-adj--ctl"></a><span data-ttu-id="abf8b-113">Ausgabe: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="abf8b-113">Output : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="abf8b-114">Ein Vorgang, der die Amplitude-Verstärkung durch Oracles implementiert, die von partiellen Reflektionen implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="abf8b-114">An operation that implements amplitude amplification by oracles that are implemented by partial reflections.</span></span>

## <a name="remarks"></a><span data-ttu-id="abf8b-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="abf8b-115">Remarks</span></span>

<span data-ttu-id="abf8b-116">Dies erzwingt strengere Bedingungen in Form von Start-und Ziel Zuständen als in `AmpAmpByReflectionPhases` .</span><span class="sxs-lookup"><span data-stu-id="abf8b-116">This imposes stricter conditions on form of the start and target states than in `AmpAmpByReflectionPhases`.</span></span>
<span data-ttu-id="abf8b-117">Es wird davon ausgegangen, dass der Ziel Status durch "$ \ket f $" gekennzeichnet ist {1} \_ .</span><span class="sxs-lookup"><span data-stu-id="abf8b-117">It is assumed that the target state is marked by $\ket{1}\_f$.</span></span>
<span data-ttu-id="abf8b-118">Es wird davon ausgegangen, dass "\begin{align} a\ket {0} \_ {f} \ket {0} \_ s = \lambda\ket {1} \_ f \ket {\ Text {Target}} \_ s + \sqrt{1-| \lambda | ^ 2} \ket {0} \_ f \ cdots" lautet, \end{align} in den meisten Fällen `flagQubit` und `auxiliaryRegister` werden im Status $ \ket {0} \_ {f} \ket {0} \_ s $ initialisiert.</span><span class="sxs-lookup"><span data-stu-id="abf8b-118">It is assumed that \begin{align} A\ket{0}\_{f}\ket{0}\_s= \lambda\ket{1}\_f\ket{\text{target}}\_s + \sqrt{1-|\lambda|^2}\ket{0}\_f\cdots, \end{align} In most cases, `flagQubit` and `auxiliaryRegister` are initialized in the state $\ket{0}\_{f}\ket{0}\_s$.</span></span>