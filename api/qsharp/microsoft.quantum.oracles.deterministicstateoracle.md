---
uid: Microsoft.Quantum.Oracles.DeterministicStateOracle
title: Benutzerdefinierter deterministicstateoracle-Typ
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: DeterministicStateOracle
qsharp.summary: >-
  Represents an oracle for deterministic state preparation.

  The input to the oracle $O$ is:

  - The register that will store the desired quantum state $\ket{\psi}\_s$.
ms.openlocfilehash: f02267d48cf42fb5b02782dc6b667ac7b60a05dc
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92724292"
---
# <a name="deterministicstateoracle-user-defined-type"></a>Benutzerdefinierter deterministicstateoracle-Typ

Namespace: [Microsoft. Quantum. Oracles](xref:Microsoft.Quantum.Oracles)

Paketen [](https://nuget.org/packages/)


Stellt ein Oracle für die deterministische Zustands Vorbereitung dar.

Die Eingabe für den Oracle-$O $ lautet wie folgt:

- Das Register, mit dem der gewünschte quantenstatus $ \ket{\psi} \_ s $ gespeichert wird.

```qsharp

newtype DeterministicStateOracle = ((Qubit[] => Unit is Adj + Ctl));
```



## <a name="remarks"></a>Hinweise

Dieses durch $O \ket {0} = \ket{\psi} $ definierte Oracle agiert auf der Grundlage des Berechnungs Zustands $ \ket {0} $ zum Erstellen des Zustands $ \ket{\psi} $.
Der erste Parameter ist das Qubit-Register von $ \ket{\psi} $.