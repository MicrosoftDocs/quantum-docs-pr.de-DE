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
# <a name="obliviousoracle-user-defined-type"></a>Benutzerdefinierter Typ "schräviousoracle"

Namespace: [Microsoft. Quantum. Oracles](xref:Microsoft.Quantum.Oracles)

Paketen [](https://nuget.org/packages/)


Stellt ein Oracle für die pervirone Amplitude-Verstärkung dar.

Die Eingaben in den Oracle-$O $ lauten:

- Der Wert von "Ancilla" wird $a $ registriert, für den $O $ agiert.
- Das System registriert $s $, auf dem der gewünschte einheitliche $U $ angewendet wird, nach der Auswahl für Register $a $ befindet sich im Status $ \ket{t} \_ a $.

```qsharp

newtype ObliviousOracle = (((Qubit[], Qubit[]) => Unit is Adj + Ctl));
```



## <a name="remarks"></a>Hinweise

Dieses Oracle ist durch $ $ o\ket {s} \_ a\ket {\ PSI} \_ s = \lambda\ket{t} \_ a U \ket{\psi} \_ s + \sqrt{1-| \lambda | ^ 2} \ket{t ^ \perp} definiert. \_ a\cdots $ $ agiert für den Ancilla State $ \ket{s} \_ a $, um die einheitliche $U $ in jedem Systemstatus $ \ket{\psi} \_ s $ mit Amplitude $ \lambda $ in der durch $ \ket{t} a $ gekennzeichneten Basis zu implementieren \_ .
Der erste Parameter ist das Qubit-Register von $ \ket{s} \_ $. Der zweite Parameter ist das Qubit-Register von $ \ket{\psi} \_ s $.