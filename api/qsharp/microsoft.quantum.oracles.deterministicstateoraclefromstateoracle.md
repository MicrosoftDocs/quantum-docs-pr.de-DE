---
uid: Microsoft.Quantum.Oracles.DeterministicStateOracleFromStateOracle
title: Deterministicstateoraclefromstateoracle-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: DeterministicStateOracleFromStateOracle
qsharp.summary: Converts an oracle of type `StateOracle` to `DeterministicStateOracle`.
ms.openlocfilehash: 183b1108ead6239e26bb0b38144cb9374e7bf285
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96226756"
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