---
uid: Microsoft.Quantum.Oracles.ObliviousOracle
title: Benutzerdefinierter Typ "schräviousoracle"
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: ObliviousOracle
qsharp.summary: >-
  Represents an oracle for oblivious amplitude amplification.

  The inputs to the oracle $O$ are:

  - The ancilla register $a$ that $O$ acts on. - The system register $s$ on which the desired unitary $U$ is applied, post-selected on register $a$ being in state $\ket{t}\_a$.
ms.openlocfilehash: 793e72af56e288f9b437302f9958665e92e5e763
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842559"
---
# <a name="obliviousoracle-user-defined-type"></a><span data-ttu-id="90698-102">Benutzerdefinierter Typ "schräviousoracle"</span><span class="sxs-lookup"><span data-stu-id="90698-102">ObliviousOracle user defined type</span></span>

<span data-ttu-id="90698-103">Namespace: [Microsoft. Quantum. Oracles](xref:Microsoft.Quantum.Oracles)</span><span class="sxs-lookup"><span data-stu-id="90698-103">Namespace: [Microsoft.Quantum.Oracles](xref:Microsoft.Quantum.Oracles)</span></span>

<span data-ttu-id="90698-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="90698-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="90698-105">Stellt ein Oracle für die pervirone Amplitude-Verstärkung dar.</span><span class="sxs-lookup"><span data-stu-id="90698-105">Represents an oracle for oblivious amplitude amplification.</span></span>

<span data-ttu-id="90698-106">Die Eingaben in den Oracle-$O $ lauten:</span><span class="sxs-lookup"><span data-stu-id="90698-106">The inputs to the oracle $O$ are:</span></span>

- <span data-ttu-id="90698-107">Der Wert von "Ancilla" wird $a $ registriert, für den $O $ agiert.</span><span class="sxs-lookup"><span data-stu-id="90698-107">The ancilla register $a$ that $O$ acts on.</span></span>
- <span data-ttu-id="90698-108">Das System registriert $s $, auf dem der gewünschte einheitliche $U $ angewendet wird, nach der Auswahl für Register $a $ befindet sich im Status $ \ket{t} \_ a $.</span><span class="sxs-lookup"><span data-stu-id="90698-108">The system register $s$ on which the desired unitary $U$ is applied, post-selected on register $a$ being in state $\ket{t}\_a$.</span></span>

```qsharp

newtype ObliviousOracle = (((Qubit[], Qubit[]) => Unit is Adj + Ctl));
```



## <a name="remarks"></a><span data-ttu-id="90698-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="90698-109">Remarks</span></span>

<span data-ttu-id="90698-110">Dieses Oracle ist durch $ $ o\ket {s} \_ a\ket {\ PSI} \_ s = \lambda\ket{t} \_ a U \ket{\psi} \_ s + \sqrt{1-| \lambda | ^ 2} \ket{t ^ \perp} definiert. \_ a\cdots $ $ agiert für den Ancilla State $ \ket{s} \_ a $, um die einheitliche $U $ in jedem Systemstatus $ \ket{\psi} \_ s $ mit Amplitude $ \lambda $ in der durch $ \ket{t} a $ gekennzeichneten Basis zu implementieren \_ .</span><span class="sxs-lookup"><span data-stu-id="90698-110">This oracle defined by $$ O\ket{s}\_a\ket{\psi}\_s= \lambda\ket{t}\_a U \ket{\psi}\_s + \sqrt{1-|\lambda|^2}\ket{t^\perp}\_a\cdots $$ acts on the ancilla state $\ket{s}\_a$ to implement the unitary $U$ on any system state $\ket{\psi}\_s$ with amplitude $\lambda$ in the basis flagged by $\ket{t}\_a$.</span></span>
<span data-ttu-id="90698-111">Der erste Parameter ist das Qubit-Register von $ \ket{s} \_ $.</span><span class="sxs-lookup"><span data-stu-id="90698-111">The first parameter is the qubit register of $\ket{s}\_a$.</span></span> <span data-ttu-id="90698-112">Der zweite Parameter ist das Qubit-Register von $ \ket{\psi} \_ s $.</span><span class="sxs-lookup"><span data-stu-id="90698-112">The second parameter is the qubit register of $\ket{\psi}\_s$.</span></span>