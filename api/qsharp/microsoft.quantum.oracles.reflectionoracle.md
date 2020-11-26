---
uid: Microsoft.Quantum.Oracles.ReflectionOracle
title: Benutzerdefinierter reflectionoracle-Typ
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: ReflectionOracle
qsharp.summary: >-
  Represents a reflection oracle.

  A reflection oracle, $O$, has inputs:

  - The phase $\phi$ by which to rotate the reflected subspace. - The qubit register on which to perform the given reflection.
ms.openlocfilehash: 7bb0626e7cca9ae0b640699ea57f2e114bda2d06
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96226654"
---
# <a name="reflectionoracle-user-defined-type"></a><span data-ttu-id="58377-102">Benutzerdefinierter reflectionoracle-Typ</span><span class="sxs-lookup"><span data-stu-id="58377-102">ReflectionOracle user defined type</span></span>

<span data-ttu-id="58377-103">Namespace: [Microsoft. Quantum. Oracles](xref:Microsoft.Quantum.Oracles)</span><span class="sxs-lookup"><span data-stu-id="58377-103">Namespace: [Microsoft.Quantum.Oracles](xref:Microsoft.Quantum.Oracles)</span></span>

<span data-ttu-id="58377-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="58377-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="58377-105">Stellt ein reflektionsinoracle dar.</span><span class="sxs-lookup"><span data-stu-id="58377-105">Represents a reflection oracle.</span></span>

<span data-ttu-id="58377-106">Ein reflektionsinoracle, $O $, weist Eingaben auf:</span><span class="sxs-lookup"><span data-stu-id="58377-106">A reflection oracle, $O$, has inputs:</span></span>

- <span data-ttu-id="58377-107">Die Phase $ \phi $, um die der reflektierte Teilbereich gedreht werden soll.</span><span class="sxs-lookup"><span data-stu-id="58377-107">The phase $\phi$ by which to rotate the reflected subspace.</span></span>
- <span data-ttu-id="58377-108">Das Qubit-Register, für das die angegebene Reflektion durchgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="58377-108">The qubit register on which to perform the given reflection.</span></span>

```qsharp

newtype ReflectionOracle = (ApplyReflection : ((Double, Qubit[]) => Unit is Adj + Ctl));
```



## <a name="named-items"></a><span data-ttu-id="58377-109">Benannte Elemente</span><span class="sxs-lookup"><span data-stu-id="58377-109">Named Items</span></span>

### <a name="applyreflection--doublequbit--unit--is-adj--ctl"></a><span data-ttu-id="58377-110">Applyreflection: ([Double](xref:microsoft.quantum.lang-ref.double),[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="58377-110">ApplyReflection : ([Double](xref:microsoft.quantum.lang-ref.double),[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>



## <a name="remarks"></a><span data-ttu-id="58377-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="58377-111">Remarks</span></span>

<span data-ttu-id="58377-112">Diese Oracle $O = \boldone-(1-e ^ {i \phi}) \ket{\psi}\bra{\psi} $ führt eine partielle Reflektion durch eine Phase $ \phi $ zu einem einzelnen reinen Status $ \ket{\psi} $ aus.</span><span class="sxs-lookup"><span data-stu-id="58377-112">This oracle $O = \boldone - (1 - e^{i \phi}) \ket{\psi}\bra{\psi}$ performs a partial reflection by a phase $\phi$ about a single pure state $\ket{\psi}$.</span></span>