---
uid: Microsoft.Quantum.AmplitudeAmplification.AmplitudeAmplificationFromPartialReflections
title: Amplitubinverstärkficationfrompartialreflections-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: AmplitudeAmplificationFromPartialReflections
qsharp.summary: Amplitude amplification by partial reflections.
ms.openlocfilehash: fc7c2c0d05ea626f7f7e5d8ebf3ce5ecea61390b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92721953"
---
# <a name="amplitudeamplificationfrompartialreflections-function"></a><span data-ttu-id="e8cef-102">Amplitubinverstärkficationfrompartialreflections-Funktion</span><span class="sxs-lookup"><span data-stu-id="e8cef-102">AmplitudeAmplificationFromPartialReflections function</span></span>

<span data-ttu-id="e8cef-103">Namespace: [Microsoft. Quantum. Verstärkungs Verstärkung](xref:Microsoft.Quantum.AmplitudeAmplification)</span><span class="sxs-lookup"><span data-stu-id="e8cef-103">Namespace: [Microsoft.Quantum.AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span></span>

<span data-ttu-id="e8cef-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="e8cef-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="e8cef-105">Amplitude-Verstärkung durch partielle Reflektionen.</span><span class="sxs-lookup"><span data-stu-id="e8cef-105">Amplitude amplification by partial reflections.</span></span>

```qsharp
function AmplitudeAmplificationFromPartialReflections (phases : Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases, startStateReflection : Microsoft.Quantum.Oracles.ReflectionOracle, targetStateReflection : Microsoft.Quantum.Oracles.ReflectionOracle) : (Qubit[] => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="e8cef-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e8cef-106">Input</span></span>

### <a name="phases--reflectionphases"></a><span data-ttu-id="e8cef-107">Phasen: [reflectionphasen](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)</span><span class="sxs-lookup"><span data-stu-id="e8cef-107">phases : [ReflectionPhases](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)</span></span>

<span data-ttu-id="e8cef-108">Phasen von partiellen Reflektionen</span><span class="sxs-lookup"><span data-stu-id="e8cef-108">Phases of partial reflections</span></span>


### <a name="startstatereflection--reflectionoracle"></a><span data-ttu-id="e8cef-109">Startstatus-eflection: [reflectionoracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)</span><span class="sxs-lookup"><span data-stu-id="e8cef-109">startStateReflection : [ReflectionOracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)</span></span>

<span data-ttu-id="e8cef-110">Reflektionsoperator zum Startstatus</span><span class="sxs-lookup"><span data-stu-id="e8cef-110">Reflection operator about start state</span></span>


### <a name="targetstatereflection--reflectionoracle"></a><span data-ttu-id="e8cef-111">targetstatuereflection: [reflectionoracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)</span><span class="sxs-lookup"><span data-stu-id="e8cef-111">targetStateReflection : [ReflectionOracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)</span></span>

<span data-ttu-id="e8cef-112">Reflektionsoperator zum Ziel Status</span><span class="sxs-lookup"><span data-stu-id="e8cef-112">Reflection operator about target state</span></span>



## <a name="output--qubit--unit-adj--ctl"></a><span data-ttu-id="e8cef-113">Ausgabe: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="e8cef-113">Output : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="e8cef-114">Ein Vorgang, der die Amplitude-Verstärkung durch partielle Reflektionen implementiert.</span><span class="sxs-lookup"><span data-stu-id="e8cef-114">An operation that implements amplitude amplification by partial reflections.</span></span>

## <a name="remarks"></a><span data-ttu-id="e8cef-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e8cef-115">Remarks</span></span>

<span data-ttu-id="e8cef-116">Die Amplitude-Verstärkung ist ein Sonderfall der Zerlegung von Amplitude, bei der keine System-Qubits vorhanden sind und das schrägende Oracle auf Identity festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="e8cef-116">Amplitude amplification is a special case of oblivious amplitude amplification where there are no system qubits and the oblivious oracle is set to identity.</span></span>
<span data-ttu-id="e8cef-117">In den meisten Fällen `startQubits` wird im Status $ \ket{\text{Start}} $1 initialisiert \_ . Dies ist der $-$1-eigen Zustand von `startStateReflection` .</span><span class="sxs-lookup"><span data-stu-id="e8cef-117">In most cases, `startQubits` is initialized in the state $\ket{\text{start}}\_1$, which is the $-1$ eigenstate of `startStateReflection`.</span></span>