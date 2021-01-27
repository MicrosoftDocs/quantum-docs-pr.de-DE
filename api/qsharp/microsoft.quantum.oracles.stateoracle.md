---
uid: Microsoft.Quantum.Oracles.StateOracle
title: Benutzerdefinierter stateoracle-Typ
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: StateOracle
qsharp.summary: >-
  Represents an oracle for state preparation.

  The inputs to the oracle $O$ are:

  - An integer indexing the flag qubit $f$. - The system register $s$ that will store the desired quantum state $\ket{\psi}\_s$.
ms.openlocfilehash: 005d7862214abb3dcb9c0caa006343720d179a52
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854468"
---
# <a name="stateoracle-user-defined-type"></a>Benutzerdefinierter stateoracle-Typ

Namespace: [Microsoft. Quantum. Oracles](xref:Microsoft.Quantum.Oracles)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Stellt ein Oracle für die Zustands Vorbereitung dar.

Die Eingaben in den Oracle-$O $ lauten:

- Eine Ganzzahl, die das Flag-Qubit $f $ indiziert.
- Das System registriert $s $, das den gewünschten Quantum-Status $ \ket{\psi} \_ s $ speichert.

```qsharp

newtype StateOracle = (((Int, Qubit[]) => Unit is Adj + Ctl));
```



## <a name="remarks"></a>Bemerkungen

Dieses Oracle ist definiert durch $ $ o\ket {0} \_ {f} \ket {0} \_ s = \lambda\ket {1} \_ f \ket {\ PSI} \_ s + \sqrt{1-| \lambda | ^ 2} \ket {0} \_ f \ cdots, $ $ agiert auf der Grundlage des Berechnungs Zustands $ \ket {0} \_ {f} \ket {0} \_ s $, um den Ziel Status $ \ket{\psi} \_ s $ mit Amplitude $ \lambda $ in der durch $ \ket {1} f $ gekennzeichneten Basis zu erstellen \_ .
Der erste Parameter ist ein Index für das Qubit-Register von $ \ket {0} \_ f $. Der zweite Parameter umfasste beide Register.