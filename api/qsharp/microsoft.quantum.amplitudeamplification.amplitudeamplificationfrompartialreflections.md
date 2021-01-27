---
uid: Microsoft.Quantum.AmplitudeAmplification.AmplitudeAmplificationFromPartialReflections
title: Amplitubinverstärkficationfrompartialreflections-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: AmplitudeAmplificationFromPartialReflections
qsharp.summary: Amplitude amplification by partial reflections.
ms.openlocfilehash: e4030aabcab55db35bcb8199e37bee837ead6ad0
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845924"
---
# <a name="amplitudeamplificationfrompartialreflections-function"></a><span data-ttu-id="98145-102">Amplitubinverstärkficationfrompartialreflections-Funktion</span><span class="sxs-lookup"><span data-stu-id="98145-102">AmplitudeAmplificationFromPartialReflections function</span></span>

<span data-ttu-id="98145-103">Namespace: [Microsoft. Quantum. Verstärkungs Verstärkung](xref:Microsoft.Quantum.AmplitudeAmplification)</span><span class="sxs-lookup"><span data-stu-id="98145-103">Namespace: [Microsoft.Quantum.AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span></span>

<span data-ttu-id="98145-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="98145-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="98145-105">Amplitude-Verstärkung durch partielle Reflektionen.</span><span class="sxs-lookup"><span data-stu-id="98145-105">Amplitude amplification by partial reflections.</span></span>

```qsharp
function AmplitudeAmplificationFromPartialReflections (phases : Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases, startStateReflection : Microsoft.Quantum.Oracles.ReflectionOracle, targetStateReflection : Microsoft.Quantum.Oracles.ReflectionOracle) : (Qubit[] => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="98145-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="98145-106">Input</span></span>

### <a name="phases--reflectionphases"></a><span data-ttu-id="98145-107">Phasen: [reflectionphasen](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)</span><span class="sxs-lookup"><span data-stu-id="98145-107">phases : [ReflectionPhases](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)</span></span>

<span data-ttu-id="98145-108">Phasen von partiellen Reflektionen</span><span class="sxs-lookup"><span data-stu-id="98145-108">Phases of partial reflections</span></span>


### <a name="startstatereflection--reflectionoracle"></a><span data-ttu-id="98145-109">Startstatus-eflection: [reflectionoracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)</span><span class="sxs-lookup"><span data-stu-id="98145-109">startStateReflection : [ReflectionOracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)</span></span>

<span data-ttu-id="98145-110">Reflektionsoperator zum Startstatus</span><span class="sxs-lookup"><span data-stu-id="98145-110">Reflection operator about start state</span></span>


### <a name="targetstatereflection--reflectionoracle"></a><span data-ttu-id="98145-111">targetstatuereflection: [reflectionoracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)</span><span class="sxs-lookup"><span data-stu-id="98145-111">targetStateReflection : [ReflectionOracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)</span></span>

<span data-ttu-id="98145-112">Reflektionsoperator zum Ziel Status</span><span class="sxs-lookup"><span data-stu-id="98145-112">Reflection operator about target state</span></span>



## <a name="output--qubit--unit--is-adj--ctl"></a><span data-ttu-id="98145-113">Ausgabe: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="98145-113">Output : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="98145-114">Ein Vorgang, der die Amplitude-Verstärkung durch partielle Reflektionen implementiert.</span><span class="sxs-lookup"><span data-stu-id="98145-114">An operation that implements amplitude amplification by partial reflections.</span></span>

## <a name="remarks"></a><span data-ttu-id="98145-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="98145-115">Remarks</span></span>

<span data-ttu-id="98145-116">Die Amplitude-Verstärkung ist ein Sonderfall der Zerlegung von Amplitude, bei der keine System-Qubits vorhanden sind und das schrägende Oracle auf Identity festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="98145-116">Amplitude amplification is a special case of oblivious amplitude amplification where there are no system qubits and the oblivious oracle is set to identity.</span></span>
<span data-ttu-id="98145-117">In den meisten Fällen `startQubits` wird im Status $ \ket{\text{Start}} $1 initialisiert \_ . Dies ist der $-$1-eigen Zustand von `startStateReflection` .</span><span class="sxs-lookup"><span data-stu-id="98145-117">In most cases, `startQubits` is initialized in the state $\ket{\text{start}}\_1$, which is the $-1$ eigenstate of `startStateReflection`.</span></span>