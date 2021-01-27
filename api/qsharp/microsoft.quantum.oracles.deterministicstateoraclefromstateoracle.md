---
uid: Microsoft.Quantum.Oracles.DeterministicStateOracleFromStateOracle
title: Deterministicstateoraclefromstateoracle-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: DeterministicStateOracleFromStateOracle
qsharp.summary: Converts an oracle of type `StateOracle` to `DeterministicStateOracle`.
ms.openlocfilehash: af545a7d6e82e654ee36ab3ba77c8f8be3384b96
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854555"
---
# <a name="deterministicstateoraclefromstateoracle-function"></a>Deterministicstateoraclefromstateoracle-Funktion

Namespace: [Microsoft. Quantum. Oracles](xref:Microsoft.Quantum.Oracles)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Konvertiert ein Oracle vom Typ `StateOracle` in `DeterministicStateOracle` .

```qsharp
function DeterministicStateOracleFromStateOracle (idxFlagQubit : Int, stateOracle : Microsoft.Quantum.Oracles.StateOracle) : Microsoft.Quantum.Oracles.DeterministicStateOracle
```


## <a name="input"></a>Eingabe

### <a name="idxflagqubit--int"></a>idxflagqubit: [int](xref:microsoft.quantum.lang-ref.int)

Der Index für das Flag-Qubit des `stateOracle` $A $, das explizit für zwei Register agiert: das Flag $f $ und das System $s $, z. b. $A \ket {0} \_ f\ket {\ PSI} \_ s $.


### <a name="stateoracle--stateoracle"></a>stateoracle: [stateoracle](xref:Microsoft.Quantum.Oracles.StateOracle)

Ein Status Vorbereitungs-Oracle $A $ vom Typ `StateOracle` .



## <a name="output--deterministicstateoracle"></a>Ausgabe: [deterministicstateoracle](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)

Die gleiche Zustands Vorbereitung ist Oracle $A $, aber jetzt vom Typ `DeterministicStateOracle` , sodass Sie auf ein Register angewendet wird, bei dem $a, s $ nicht mehr explizit getrennt werden, z. b.  $A \ket{0\psi} \_ {As} $.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Oracles. stateoracle](xref:Microsoft.Quantum.Oracles.StateOracle)
- [Microsoft. Quantum. Oracles. deterministicstateoracle](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)