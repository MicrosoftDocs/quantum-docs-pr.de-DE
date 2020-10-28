---
uid: Microsoft.Quantum.Oracles.StateOracleFromDeterministicStateOracle
title: Stateoraclefromdeterministicstateoracle-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: StateOracleFromDeterministicStateOracle
qsharp.summary: Converts an oracle of type `DeterministicStateOracle` to `StateOracle`.
ms.openlocfilehash: ccb083dbaaec2f306ba0740ef364ebb22408ed98
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92724221"
---
# <a name="stateoraclefromdeterministicstateoracle-function"></a>Stateoraclefromdeterministicstateoracle-Funktion

Namespace: [Microsoft. Quantum. Oracles](xref:Microsoft.Quantum.Oracles)

Paketen [](https://nuget.org/packages/)


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