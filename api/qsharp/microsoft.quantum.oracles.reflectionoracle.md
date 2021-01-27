---
uid: Microsoft.Quantum.Oracles.ReflectionOracle
title: Benutzerdefinierter reflectionoracle-Typ
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: ReflectionOracle
qsharp.summary: >-
  Represents a reflection oracle.

  A reflection oracle, $O$, has inputs:

  - The phase $\phi$ by which to rotate the reflected subspace. - The qubit register on which to perform the given reflection.
ms.openlocfilehash: 1ef07126596b70d2c5574430656009116c34d2bc
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854491"
---
# <a name="reflectionoracle-user-defined-type"></a><span data-ttu-id="12754-102">Benutzerdefinierter reflectionoracle-Typ</span><span class="sxs-lookup"><span data-stu-id="12754-102">ReflectionOracle user defined type</span></span>

<span data-ttu-id="12754-103">Namespace: [Microsoft. Quantum. Oracles](xref:Microsoft.Quantum.Oracles)</span><span class="sxs-lookup"><span data-stu-id="12754-103">Namespace: [Microsoft.Quantum.Oracles](xref:Microsoft.Quantum.Oracles)</span></span>

<span data-ttu-id="12754-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="12754-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="12754-105">Stellt ein reflektionsinoracle dar.</span><span class="sxs-lookup"><span data-stu-id="12754-105">Represents a reflection oracle.</span></span>

<span data-ttu-id="12754-106">Ein reflektionsinoracle, $O $, weist Eingaben auf:</span><span class="sxs-lookup"><span data-stu-id="12754-106">A reflection oracle, $O$, has inputs:</span></span>

- <span data-ttu-id="12754-107">Die Phase $ \phi $, um die der reflektierte Teilbereich gedreht werden soll.</span><span class="sxs-lookup"><span data-stu-id="12754-107">The phase $\phi$ by which to rotate the reflected subspace.</span></span>
- <span data-ttu-id="12754-108">Das Qubit-Register, für das die angegebene Reflektion durchgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="12754-108">The qubit register on which to perform the given reflection.</span></span>

```qsharp

newtype ReflectionOracle = (ApplyReflection : ((Double, Qubit[]) => Unit is Adj + Ctl));
```



## <a name="named-items"></a><span data-ttu-id="12754-109">Benannte Elemente</span><span class="sxs-lookup"><span data-stu-id="12754-109">Named Items</span></span>

### <a name="applyreflection--doublequbit--unit--is-adj--ctl"></a><span data-ttu-id="12754-110">Applyreflection: ([Double](xref:microsoft.quantum.lang-ref.double),[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="12754-110">ApplyReflection : ([Double](xref:microsoft.quantum.lang-ref.double),[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>



## <a name="remarks"></a><span data-ttu-id="12754-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="12754-111">Remarks</span></span>

<span data-ttu-id="12754-112">Diese Oracle $O = \boldone-(1-e ^ {i \phi}) \ket{\psi}\bra{\psi} $ führt eine partielle Reflektion durch eine Phase $ \phi $ zu einem einzelnen reinen Status $ \ket{\psi} $ aus.</span><span class="sxs-lookup"><span data-stu-id="12754-112">This oracle $O = \boldone - (1 - e^{i \phi}) \ket{\psi}\bra{\psi}$ performs a partial reflection by a phase $\phi$ about a single pure state $\ket{\psi}$.</span></span>