---
uid: Microsoft.Quantum.Oracles.ReflectionOracle
title: Benutzerdefinierter reflectionoracle-Typ
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: ReflectionOracle
qsharp.summary: >-
  Represents a reflection oracle.

  A reflection oracle, $O$, has inputs:

  - The phase $\phi$ by which to rotate the reflected subspace. - The qubit register on which to perform the given reflection.
ms.openlocfilehash: 8e35e7e508ea7e0c30ea2a70633f71a6c87d4be1
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92724208"
---
# <a name="reflectionoracle-user-defined-type"></a><span data-ttu-id="8f2c5-102">Benutzerdefinierter reflectionoracle-Typ</span><span class="sxs-lookup"><span data-stu-id="8f2c5-102">ReflectionOracle user defined type</span></span>

<span data-ttu-id="8f2c5-103">Namespace: [Microsoft. Quantum. Oracles](xref:Microsoft.Quantum.Oracles)</span><span class="sxs-lookup"><span data-stu-id="8f2c5-103">Namespace: [Microsoft.Quantum.Oracles](xref:Microsoft.Quantum.Oracles)</span></span>

<span data-ttu-id="8f2c5-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="8f2c5-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="8f2c5-105">Stellt ein reflektionsinoracle dar.</span><span class="sxs-lookup"><span data-stu-id="8f2c5-105">Represents a reflection oracle.</span></span>

<span data-ttu-id="8f2c5-106">Ein reflektionsinoracle, $O $, weist Eingaben auf:</span><span class="sxs-lookup"><span data-stu-id="8f2c5-106">A reflection oracle, $O$, has inputs:</span></span>

- <span data-ttu-id="8f2c5-107">Die Phase $ \phi $, um die der reflektierte Teilbereich gedreht werden soll.</span><span class="sxs-lookup"><span data-stu-id="8f2c5-107">The phase $\phi$ by which to rotate the reflected subspace.</span></span>
- <span data-ttu-id="8f2c5-108">Das Qubit-Register, für das die angegebene Reflektion durchgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="8f2c5-108">The qubit register on which to perform the given reflection.</span></span>

```qsharp

newtype ReflectionOracle = (ApplyReflection : ((Double, Qubit[]) => Unit is Adj + Ctl));
```



## <a name="named-items"></a><span data-ttu-id="8f2c5-109">Benannte Elemente</span><span class="sxs-lookup"><span data-stu-id="8f2c5-109">Named Items</span></span>

### <a name="applyreflection--doublequbit--unit-adj--ctl"></a><span data-ttu-id="8f2c5-110">Applyreflection: ([Double](xref:microsoft.quantum.lang-ref.double),[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="8f2c5-110">ApplyReflection : ([Double](xref:microsoft.quantum.lang-ref.double),[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>



## <a name="remarks"></a><span data-ttu-id="8f2c5-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8f2c5-111">Remarks</span></span>

<span data-ttu-id="8f2c5-112">Diese Oracle $O = \boldone-(1-e ^ {i \phi}) \ket{\psi}\bra{\psi} $ führt eine partielle Reflektion durch eine Phase $ \phi $ zu einem einzelnen reinen Status $ \ket{\psi} $ aus.</span><span class="sxs-lookup"><span data-stu-id="8f2c5-112">This oracle $O = \boldone - (1 - e^{i \phi}) \ket{\psi}\bra{\psi}$ performs a partial reflection by a phase $\phi$ about a single pure state $\ket{\psi}$.</span></span>