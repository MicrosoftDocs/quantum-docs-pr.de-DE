---
uid: Microsoft.Quantum.Diagnostics.AssertPhase
title: Assertphase-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertPhase
qsharp.summary: Asserts that the phase of an equal superposition state has the expected value.
ms.openlocfilehash: 59fa0f2f68b4de271b972aef776ee5097fd5c201
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98830078"
---
# <a name="assertphase-operation"></a><span data-ttu-id="b2122-102">Assertphase-Vorgang</span><span class="sxs-lookup"><span data-stu-id="b2122-102">AssertPhase operation</span></span>

<span data-ttu-id="b2122-103">Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="b2122-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="b2122-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="b2122-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="b2122-105">Bestätigt, dass die Phase eines gleich geordneten Superposition-Zustands den erwarteten Wert aufweist.</span><span class="sxs-lookup"><span data-stu-id="b2122-105">Asserts that the phase of an equal superposition state has the expected value.</span></span>

```qsharp
operation AssertPhase (expected : Double, qubit : Qubit, tolerance : Double) : Unit
```


## <a name="description"></a><span data-ttu-id="b2122-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b2122-106">Description</span></span>

<span data-ttu-id="b2122-107">Dieser Vorgang bestätigt, dass die Phase $ \phi $ eines Quantum-Zustands, der als $ \bruchteil {e ^ {i t}} {\sqrt {2} } (e ^ {i\phi} \ Ket {0} + e ^ {-i\phi} \ Ket + e ^ {-i\phi} \ Ket) $ ausgedrückt werden kann, {1} für eine beliebige reale $t $ den erwarteten</span><span class="sxs-lookup"><span data-stu-id="b2122-107">This operation asserts that the phase $\phi$ of a quantum state that may be expressed as $\frac{e^{i t}}{\sqrt{2}}(e^{i\phi}\ket{0} + e^{-i\phi}\ket{1})$ for some arbitrary real $t$ has the expected value.</span></span>

## <a name="input"></a><span data-ttu-id="b2122-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b2122-108">Input</span></span>

### <a name="expected--double"></a><span data-ttu-id="b2122-109">erwartet: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="b2122-109">expected : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="b2122-110">Der erwartete Wert von "$ \phi \in" (-\pi, \pi] $.</span><span class="sxs-lookup"><span data-stu-id="b2122-110">The expected value of $\phi \in (-\pi,\pi]$.</span></span>


### <a name="qubit--qubit"></a><span data-ttu-id="b2122-111">Qubit: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="b2122-111">qubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="b2122-112">Das Qubit, das den erwarteten Zustand speichert.</span><span class="sxs-lookup"><span data-stu-id="b2122-112">The qubit that stores the expected state.</span></span>


### <a name="tolerance--double"></a><span data-ttu-id="b2122-113">Toleranz: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="b2122-113">tolerance : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="b2122-114">Absolute Toleranz für den Unterschied zwischen tatsächlichem und erwartetem Verhalten.</span><span class="sxs-lookup"><span data-stu-id="b2122-114">Absolute tolerance on the difference between actual and expected.</span></span>



## <a name="output--unit"></a><span data-ttu-id="b2122-115">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="b2122-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="example"></a><span data-ttu-id="b2122-116">Beispiel</span><span class="sxs-lookup"><span data-stu-id="b2122-116">Example</span></span>

<span data-ttu-id="b2122-117">Der folgende Assert ist erfolgreich: `qubit` befindet sich im Zustand $ \ket{\psi} = e ^ {i 0,5} \ sqrt {1/2} \ Ket {0} + e ^ {i 0,5} \ sqrt {1/2} \ Ket {1} $;</span><span class="sxs-lookup"><span data-stu-id="b2122-117">The following assert succeeds: `qubit` is in state $\ket{\psi}=e^{i 0.5}\sqrt{1/2}\ket{0}+e^{i 0.5}\sqrt{1/2}\ket{1}$;</span></span>

- `AssertPhase(0.0,qubit,10e-10);`

<span data-ttu-id="b2122-118">`qubit` befindet sich im Status $ \ket{\psi} = e ^ {i 0,5} \ sqrt {1/2} \ Ket {0} + e ^ {-i 0,5} \ sqrt {1/2} \ Ket {1} $;</span><span class="sxs-lookup"><span data-stu-id="b2122-118">`qubit` is in state $\ket{\psi}=e^{i 0.5}\sqrt{1/2}\ket{0}+e^{-i 0.5}\sqrt{1/2}\ket{1}$;</span></span>

- `AssertPhase(0.5,qubit,10e-10);`

<span data-ttu-id="b2122-119">`qubit` befindet sich im Status $ \ket{\psi} = e ^ {-i 2.2} \ sqrt {1/2} \ Ket {0} + e ^ {i 0,2} \ sqrt {1/2} \ Ket {1} $;</span><span class="sxs-lookup"><span data-stu-id="b2122-119">`qubit` is in state $\ket{\psi}=e^{-i 2.2}\sqrt{1/2}\ket{0}+e^{i 0.2}\sqrt{1/2}\ket{1}$;</span></span>

- `AssertPhase(-1.2,qubit,10e-10);`