---
uid: Microsoft.Quantum.Oracles.StateOracleFromDeterministicStateOracle
title: Stateoraclefromdeterministicstateoracle-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: StateOracleFromDeterministicStateOracle
qsharp.summary: Converts an oracle of type `DeterministicStateOracle` to `StateOracle`.
ms.openlocfilehash: f3c225ee185b4b70ab0ea60af6f0fb154288d9bf
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96193810"
---
# <a name="stateoraclefromdeterministicstateoracle-function"></a>Stateoraclefromdeterministicstateoracle-Funktion

Namespace: [Microsoft. Quantum. Oracles](xref:Microsoft.Quantum.Oracles)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Konvertiert ein Oracle vom Typ `DeterministicStateOracle` in `StateOracle` .

```qsharp
function StateOracleFromDeterministicStateOracle (deterministicStateOracle : Microsoft.Quantum.Oracles.DeterministicStateOracle) : Microsoft.Quantum.Oracles.StateOracle
```


## <a name="input"></a>Eingabe

### <a name="deterministicstateoracle--deterministicstateoracle"></a>deterministicstateoracle: [deterministicstateoracle](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)

Ein Status Vorbereitungs-Oracle $A $ vom Typ `DeterministicStateOracle` .



## <a name="output--stateoracle"></a>Ausgabe: [stateoracle](xref:Microsoft.Quantum.Oracles.StateOracle)

Das gleiche Zustands Vorbereitungs-Oracle $A $, aber jetzt vom Typ `StateOracle` . Beachten Sie, dass der FlagIndex in dieser `StateOracle` eine Dummyvariable ist und keine Auswirkung hat.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Oracles. deterministicstateoracle](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)
- [Microsoft. Quantum. Oracles. stateoracle](xref:Microsoft.Quantum.Oracles.StateOracle)