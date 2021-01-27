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
# <a name="deterministicstateoracle-user-defined-type"></a>Benutzerdefinierter deterministicstateoracle-Typ

Namespace: [Microsoft. Quantum. Oracles](xref:Microsoft.Quantum.Oracles)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Stellt ein Oracle für die deterministische Zustands Vorbereitung dar.

Die Eingabe für den Oracle-$O $ lautet wie folgt:

- Das Register, mit dem der gewünschte quantenstatus $ \ket{\psi} \_ s $ gespeichert wird.

```qsharp

newtype DeterministicStateOracle = ((Qubit[] => Unit is Adj + Ctl));
```



## <a name="remarks"></a>Bemerkungen

Dieses durch $O \ket {0} = \ket{\psi} $ definierte Oracle agiert auf der Grundlage des Berechnungs Zustands $ \ket {0} $ zum Erstellen des Zustands $ \ket{\psi} $.
Der erste Parameter ist das Qubit-Register von $ \ket{\psi} $.