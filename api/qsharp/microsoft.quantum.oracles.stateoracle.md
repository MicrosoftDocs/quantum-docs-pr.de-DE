---
uid: Microsoft.Quantum.Oracles.StateOracle
title: Benutzerdefinierter stateoracle-Typ
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: StateOracle
qsharp.summary: >-
  Represents an oracle for state preparation.

  The inputs to the oracle $O$ are:

  - An integer indexing the flag qubit $f$. - The system register $s$ that will store the desired quantum state $\ket{\psi}\_s$.
ms.openlocfilehash: 65f4edcf2101190da0c6d00eb4dd21881143ceb0
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92724222"
---
# <a name="stateoracle-user-defined-type"></a><span data-ttu-id="add2f-102">Benutzerdefinierter stateoracle-Typ</span><span class="sxs-lookup"><span data-stu-id="add2f-102">StateOracle user defined type</span></span>

<span data-ttu-id="add2f-103">Namespace: [Microsoft. Quantum. Oracles](xref:Microsoft.Quantum.Oracles)</span><span class="sxs-lookup"><span data-stu-id="add2f-103">Namespace: [Microsoft.Quantum.Oracles](xref:Microsoft.Quantum.Oracles)</span></span>

<span data-ttu-id="add2f-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="add2f-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="add2f-105">Stellt ein Oracle für die Zustands Vorbereitung dar.</span><span class="sxs-lookup"><span data-stu-id="add2f-105">Represents an oracle for state preparation.</span></span>

<span data-ttu-id="add2f-106">Die Eingaben in den Oracle-$O $ lauten:</span><span class="sxs-lookup"><span data-stu-id="add2f-106">The inputs to the oracle $O$ are:</span></span>

- <span data-ttu-id="add2f-107">Eine Ganzzahl, die das Flag-Qubit $f $ indiziert.</span><span class="sxs-lookup"><span data-stu-id="add2f-107">An integer indexing the flag qubit $f$.</span></span>
- <span data-ttu-id="add2f-108">Das System registriert $s $, das den gewünschten Quantum-Status $ \ket{\psi} \_ s $ speichert.</span><span class="sxs-lookup"><span data-stu-id="add2f-108">The system register $s$ that will store the desired quantum state $\ket{\psi}\_s$.</span></span>

```qsharp

newtype StateOracle = (((Int, Qubit[]) => Unit is Adj + Ctl));
```



## <a name="remarks"></a><span data-ttu-id="add2f-109">Hinweise</span><span class="sxs-lookup"><span data-stu-id="add2f-109">Remarks</span></span>

<span data-ttu-id="add2f-110">Dieses Oracle ist definiert durch $ $ o\ket {0} \_ {f} \ket {0} \_ s = \lambda\ket {1} \_ f \ket {\ PSI} \_ s + \sqrt{1-| \lambda | ^ 2} \ket {0} \_ f \ cdots, $ $ agiert auf der Grundlage des Berechnungs Zustands $ \ket {0} \_ {f} \ket {0} \_ s $, um den Ziel Status $ \ket{\psi} \_ s $ mit Amplitude $ \lambda $ in der durch $ \ket {1} f $ gekennzeichneten Basis zu erstellen \_ .</span><span class="sxs-lookup"><span data-stu-id="add2f-110">This oracle defined by $$ O\ket{0}\_{f}\ket{0}\_s= \lambda\ket{1}\_f\ket{\psi}\_s + \sqrt{1-|\lambda|^2}\ket{0}\_f\cdots, $$ acts on the on computational basis state $\ket{0}\_{f}\ket{0}\_s$ to create the target state $\ket{\psi}\_s$ with amplitude $\lambda$ in the basis flagged by $\ket{1}\_f$.</span></span>
<span data-ttu-id="add2f-111">Der erste Parameter ist ein Index für das Qubit-Register von $ \ket {0} \_ f $.</span><span class="sxs-lookup"><span data-stu-id="add2f-111">The first parameter is an index to the qubit register of $\ket{0}\_f$.</span></span> <span data-ttu-id="add2f-112">Der zweite Parameter umfasste beide Register.</span><span class="sxs-lookup"><span data-stu-id="add2f-112">The second parameter encompassed both registers.</span></span>