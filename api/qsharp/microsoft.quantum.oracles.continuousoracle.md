---
uid: Microsoft.Quantum.Oracles.ContinuousOracle
title: Continuousoracle-benutzerdefinierter Typ
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: ContinuousOracle
qsharp.summary: >-
  Represents a continuous-time oracle.

  This is an oracle that implements $U(\delta t) : \ket{\psi(t)} \mapsto \ket{\psi(t + \delta t)}$ for all times $t$, where $U$ is a fixed operation, and where $\delta t$ is a non-negative real number.
ms.openlocfilehash: 9bc9b4bbdab6905a6a79893b1d559425ac679400
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92724319"
---
# <a name="continuousoracle-user-defined-type"></a>Continuousoracle-benutzerdefinierter Typ

Namespace: [Microsoft. Quantum. Oracles](xref:Microsoft.Quantum.Oracles)

Paketen [](https://nuget.org/packages/)


Stellt ein kontinuierliches Oracle dar.

Dies ist ein Oracle, das $U (\delta t): \ket{\psi (t)} \mapsto \ket{\psi (t + \delta t)} $ für alle Male $t $ implementiert, wobei $U $ ein fester Vorgang ist und $ \delta t $ eine nicht negative reelle Zahl ist.

```qsharp

newtype ContinuousOracle = (((Double, Qubit[]) => Unit is Adj + Ctl));
```

