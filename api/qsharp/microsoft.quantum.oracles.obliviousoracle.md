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
# <a name="obliviousoracle-user-defined-type"></a>Benutzerdefinierter Typ "schräviousoracle"

Namespace: [Microsoft. Quantum. Oracles](xref:Microsoft.Quantum.Oracles)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Stellt ein Oracle für die pervirone Amplitude-Verstärkung dar.

Die Eingaben in den Oracle-$O $ lauten:

- Der Wert von "Ancilla" wird $a $ registriert, für den $O $ agiert.
- Das System registriert $s $, auf dem der gewünschte einheitliche $U $ angewendet wird, nach der Auswahl für Register $a $ befindet sich im Status $ \ket{t} \_ a $.

```qsharp

newtype ObliviousOracle = (((Qubit[], Qubit[]) => Unit is Adj + Ctl));
```



## <a name="remarks"></a>Bemerkungen

Dieses Oracle ist durch $ $ o\ket {s} \_ a\ket {\ PSI} \_ s = \lambda\ket{t} \_ a U \ket{\psi} \_ s + \sqrt{1-| \lambda | ^ 2} \ket{t ^ \perp} definiert. \_ a\cdots $ $ agiert für den Ancilla State $ \ket{s} \_ a $, um die einheitliche $U $ in jedem Systemstatus $ \ket{\psi} \_ s $ mit Amplitude $ \lambda $ in der durch $ \ket{t} a $ gekennzeichneten Basis zu implementieren \_ .
Der erste Parameter ist das Qubit-Register von $ \ket{s} \_ $. Der zweite Parameter ist das Qubit-Register von $ \ket{\psi} \_ s $.