---
uid: Microsoft.Quantum.Oracles.DiscreteOracle
title: Benutzerdefinierter Typ "diskreteoracle"
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: DiscreteOracle
qsharp.summary: >-
  Represents a discrete-time oracle.

  This is an oracle that implements $U^m$ for a fixed operation $U$ and a non-negative integer $m$.
ms.openlocfilehash: ccbcc92d4b6f1c800b576ad54739d26665e6d6d5
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92724922"
---
# <a name="discreteoracle-user-defined-type"></a>Benutzerdefinierter Typ "diskreteoracle"

Namespace: [Microsoft. Quantum. Oracles](xref:Microsoft.Quantum.Oracles)

Paketen [](https://nuget.org/packages/)


Stellt ein diskretes Oracle dar.

Dies ist ein Oracle, das $U ^ m $ für einen Fixed-Vorgang implementiert $U $ und eine nicht negative ganze Zahl $m $.

```qsharp

newtype DiscreteOracle = (((Int, Qubit[]) => Unit is Adj + Ctl));
```

