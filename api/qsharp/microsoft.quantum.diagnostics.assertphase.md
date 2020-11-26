---
uid: Microsoft.Quantum.Diagnostics.AssertPhase
title: Assertphase-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertPhase
qsharp.summary: Asserts that the phase of an equal superposition state has the expected value.
ms.openlocfilehash: 9130d6c735d90abbc51989ef4a68a8eff8b41371
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96202259"
---
# <a name="assertphase-operation"></a><span data-ttu-id="29170-102">Assertphase-Vorgang</span><span class="sxs-lookup"><span data-stu-id="29170-102">AssertPhase operation</span></span>

<span data-ttu-id="29170-103">Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="29170-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="29170-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="29170-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="29170-105">Bestätigt, dass die Phase eines gleich geordneten Superposition-Zustands den erwarteten Wert aufweist.</span><span class="sxs-lookup"><span data-stu-id="29170-105">Asserts that the phase of an equal superposition state has the expected value.</span></span>

```qsharp
operation AssertPhase (expected : Double, qubit : Qubit, tolerance : Double) : Unit
```


## <a name="description"></a><span data-ttu-id="29170-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="29170-106">Description</span></span>

<span data-ttu-id="29170-107">Dieser Vorgang bestätigt, dass die Phase $ \phi $ eines Quantum-Zustands, der als $ \bruchteil {e ^ {i t}} {\sqrt {2} } (e ^ {i\phi} \ Ket {0} + e ^ {-i\phi} \ Ket + e ^ {-i\phi} \ Ket) $ ausgedrückt werden kann, {1} für eine beliebige reale $t $ den erwarteten</span><span class="sxs-lookup"><span data-stu-id="29170-107">This operation asserts that the phase $\phi$ of a quantum state that may be expressed as $\frac{e^{i t}}{\sqrt{2}}(e^{i\phi}\ket{0} + e^{-i\phi}\ket{1})$ for some arbitrary real $t$ has the expected value.</span></span>

## <a name="input"></a><span data-ttu-id="29170-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="29170-108">Input</span></span>

### <a name="expected--double"></a><span data-ttu-id="29170-109">erwartet: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="29170-109">expected : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="29170-110">Der erwartete Wert von "$ \phi \in" (-\pi, \pi] $.</span><span class="sxs-lookup"><span data-stu-id="29170-110">The expected value of $\phi \in (-\pi,\pi]$.</span></span>


### <a name="qubit--qubit"></a><span data-ttu-id="29170-111">Qubit: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="29170-111">qubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="29170-112">Das Qubit, das den erwarteten Zustand speichert.</span><span class="sxs-lookup"><span data-stu-id="29170-112">The qubit that stores the expected state.</span></span>


### <a name="tolerance--double"></a><span data-ttu-id="29170-113">Toleranz: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="29170-113">tolerance : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="29170-114">Absolute Toleranz für den Unterschied zwischen tatsächlichem und erwartetem Verhalten.</span><span class="sxs-lookup"><span data-stu-id="29170-114">Absolute tolerance on the difference between actual and expected.</span></span>



## <a name="output--unit"></a><span data-ttu-id="29170-115">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="29170-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

