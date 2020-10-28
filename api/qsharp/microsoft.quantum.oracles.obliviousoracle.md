---
uid: Microsoft.Quantum.Oracles.ObliviousOracle
title: Benutzerdefinierter Typ "schräviousoracle"
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: ObliviousOracle
qsharp.summary: >-
  Represents an oracle for oblivious amplitude amplification.

  The inputs to the oracle $O$ are:

  - The ancilla register $a$ that $O$ acts on. - The system register $s$ on which the desired unitary $U$ is applied, post-selected on register $a$ being in state $\ket{t}\_a$.
ms.openlocfilehash: 7c5b35984f3c8828a5ba9bdae8f9effbc1d378f2
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92701904"
---
# <a name="obliviousoracle-user-defined-type"></a><span data-ttu-id="f3022-102">Benutzerdefinierter Typ "schräviousoracle"</span><span class="sxs-lookup"><span data-stu-id="f3022-102">ObliviousOracle user defined type</span></span>

<span data-ttu-id="f3022-103">Namespace: [Microsoft. Quantum. Oracles](xref:Microsoft.Quantum.Oracles)</span><span class="sxs-lookup"><span data-stu-id="f3022-103">Namespace: [Microsoft.Quantum.Oracles](xref:Microsoft.Quantum.Oracles)</span></span>

<span data-ttu-id="f3022-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="f3022-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="f3022-105">Stellt ein Oracle für die pervirone Amplitude-Verstärkung dar.</span><span class="sxs-lookup"><span data-stu-id="f3022-105">Represents an oracle for oblivious amplitude amplification.</span></span>

<span data-ttu-id="f3022-106">Die Eingaben in den Oracle-$O $ lauten:</span><span class="sxs-lookup"><span data-stu-id="f3022-106">The inputs to the oracle $O$ are:</span></span>

- <span data-ttu-id="f3022-107">Der Wert von "Ancilla" wird $a $ registriert, für den $O $ agiert.</span><span class="sxs-lookup"><span data-stu-id="f3022-107">The ancilla register $a$ that $O$ acts on.</span></span>
- <span data-ttu-id="f3022-108">Das System registriert $s $, auf dem der gewünschte einheitliche $U $ angewendet wird, nach der Auswahl für Register $a $ befindet sich im Status $ \ket{t} \_ a $.</span><span class="sxs-lookup"><span data-stu-id="f3022-108">The system register $s$ on which the desired unitary $U$ is applied, post-selected on register $a$ being in state $\ket{t}\_a$.</span></span>

```qsharp

newtype ObliviousOracle = (((Qubit[], Qubit[]) => Unit is Adj + Ctl));
```



## <a name="remarks"></a><span data-ttu-id="f3022-109">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f3022-109">Remarks</span></span>

<span data-ttu-id="f3022-110">Dieses Oracle ist durch $ $ o\ket {s} \_ a\ket {\ PSI} \_ s = \lambda\ket{t} \_ a U \ket{\psi} \_ s + \sqrt{1-| \lambda | ^ 2} \ket{t ^ \perp} definiert. \_ a\cdots $ $ agiert für den Ancilla State $ \ket{s} \_ a $, um die einheitliche $U $ in jedem Systemstatus $ \ket{\psi} \_ s $ mit Amplitude $ \lambda $ in der durch $ \ket{t} a $ gekennzeichneten Basis zu implementieren \_ .</span><span class="sxs-lookup"><span data-stu-id="f3022-110">This oracle defined by $$ O\ket{s}\_a\ket{\psi}\_s= \lambda\ket{t}\_a U \ket{\psi}\_s + \sqrt{1-|\lambda|^2}\ket{t^\perp}\_a\cdots $$ acts on the ancilla state $\ket{s}\_a$ to implement the unitary $U$ on any system state $\ket{\psi}\_s$ with amplitude $\lambda$ in the basis flagged by $\ket{t}\_a$.</span></span>
<span data-ttu-id="f3022-111">Der erste Parameter ist das Qubit-Register von $ \ket{s} \_ $.</span><span class="sxs-lookup"><span data-stu-id="f3022-111">The first parameter is the qubit register of $\ket{s}\_a$.</span></span> <span data-ttu-id="f3022-112">Der zweite Parameter ist das Qubit-Register von $ \ket{\psi} \_ s $.</span><span class="sxs-lookup"><span data-stu-id="f3022-112">The second parameter is the qubit register of $\ket{\psi}\_s$.</span></span>