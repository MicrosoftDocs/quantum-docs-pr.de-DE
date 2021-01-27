---
uid: Microsoft.Quantum.Oracles.DeterministicStateOracle
title: Benutzerdefinierter deterministicstateoracle-Typ
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: DeterministicStateOracle
qsharp.summary: >-
  Represents an oracle for deterministic state preparation.

  The input to the oracle $O$ is:

  - The register that will store the desired quantum state $\ket{\psi}\_s$.
ms.openlocfilehash: 10ae9e52f298cdfb92dd6a9e5cf85960bece6800
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842587"
---
# <a name="deterministicstateoracle-user-defined-type"></a><span data-ttu-id="7be1e-102">Benutzerdefinierter deterministicstateoracle-Typ</span><span class="sxs-lookup"><span data-stu-id="7be1e-102">DeterministicStateOracle user defined type</span></span>

<span data-ttu-id="7be1e-103">Namespace: [Microsoft. Quantum. Oracles](xref:Microsoft.Quantum.Oracles)</span><span class="sxs-lookup"><span data-stu-id="7be1e-103">Namespace: [Microsoft.Quantum.Oracles](xref:Microsoft.Quantum.Oracles)</span></span>

<span data-ttu-id="7be1e-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="7be1e-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="7be1e-105">Stellt ein Oracle für die deterministische Zustands Vorbereitung dar.</span><span class="sxs-lookup"><span data-stu-id="7be1e-105">Represents an oracle for deterministic state preparation.</span></span>

<span data-ttu-id="7be1e-106">Die Eingabe für den Oracle-$O $ lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="7be1e-106">The input to the oracle $O$ is:</span></span>

- <span data-ttu-id="7be1e-107">Das Register, mit dem der gewünschte quantenstatus $ \ket{\psi} \_ s $ gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="7be1e-107">The register that will store the desired quantum state $\ket{\psi}\_s$.</span></span>

```qsharp

newtype DeterministicStateOracle = ((Qubit[] => Unit is Adj + Ctl));
```



## <a name="remarks"></a><span data-ttu-id="7be1e-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7be1e-108">Remarks</span></span>

<span data-ttu-id="7be1e-109">Dieses durch $O \ket {0} = \ket{\psi} $ definierte Oracle agiert auf der Grundlage des Berechnungs Zustands $ \ket {0} $ zum Erstellen des Zustands $ \ket{\psi} $.</span><span class="sxs-lookup"><span data-stu-id="7be1e-109">This oracle defined by $O\ket{0}=\ket{\psi}$ acts on the on computational basis state $\ket{0}$ to create the state $\ket{\psi}$.</span></span>
<span data-ttu-id="7be1e-110">Der erste Parameter ist das Qubit-Register von $ \ket{\psi} $.</span><span class="sxs-lookup"><span data-stu-id="7be1e-110">The first parameter is the qubit register of $\ket{\psi}$.</span></span>