---
uid: Microsoft.Quantum.Oracles.DeterministicStateOracle
title: Benutzerdefinierter deterministicstateoracle-Typ
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: DeterministicStateOracle
qsharp.summary: >-
  Represents an oracle for deterministic state preparation.

  The input to the oracle $O$ is:

  - The register that will store the desired quantum state $\ket{\psi}\_s$.
ms.openlocfilehash: 6f8f80aacd3386ba61675101acb87e09fff5afff
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96193929"
---
# <a name="deterministicstateoracle-user-defined-type"></a><span data-ttu-id="4ab96-102">Benutzerdefinierter deterministicstateoracle-Typ</span><span class="sxs-lookup"><span data-stu-id="4ab96-102">DeterministicStateOracle user defined type</span></span>

<span data-ttu-id="4ab96-103">Namespace: [Microsoft. Quantum. Oracles](xref:Microsoft.Quantum.Oracles)</span><span class="sxs-lookup"><span data-stu-id="4ab96-103">Namespace: [Microsoft.Quantum.Oracles](xref:Microsoft.Quantum.Oracles)</span></span>

<span data-ttu-id="4ab96-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="4ab96-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="4ab96-105">Stellt ein Oracle für die deterministische Zustands Vorbereitung dar.</span><span class="sxs-lookup"><span data-stu-id="4ab96-105">Represents an oracle for deterministic state preparation.</span></span>

<span data-ttu-id="4ab96-106">Die Eingabe für den Oracle-$O $ lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="4ab96-106">The input to the oracle $O$ is:</span></span>

- <span data-ttu-id="4ab96-107">Das Register, mit dem der gewünschte quantenstatus $ \ket{\psi} \_ s $ gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="4ab96-107">The register that will store the desired quantum state $\ket{\psi}\_s$.</span></span>

```qsharp

newtype DeterministicStateOracle = ((Qubit[] => Unit is Adj + Ctl));
```



## <a name="remarks"></a><span data-ttu-id="4ab96-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4ab96-108">Remarks</span></span>

<span data-ttu-id="4ab96-109">Dieses durch $O \ket {0} = \ket{\psi} $ definierte Oracle agiert auf der Grundlage des Berechnungs Zustands $ \ket {0} $ zum Erstellen des Zustands $ \ket{\psi} $.</span><span class="sxs-lookup"><span data-stu-id="4ab96-109">This oracle defined by $O\ket{0}=\ket{\psi}$ acts on the on computational basis state $\ket{0}$ to create the state $\ket{\psi}$.</span></span>
<span data-ttu-id="4ab96-110">Der erste Parameter ist das Qubit-Register von $ \ket{\psi} $.</span><span class="sxs-lookup"><span data-stu-id="4ab96-110">The first parameter is the qubit register of $\ket{\psi}$.</span></span>