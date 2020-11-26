---
uid: Microsoft.Quantum.Oracles.ObliviousOracleFromDeterministicStateOracle
title: Obliviousoraclefromdeterministicstateoracle-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: ObliviousOracleFromDeterministicStateOracle
qsharp.summary: Combines the oracles `DeterministicStateOracle` and `ObliviousOracle`.
ms.openlocfilehash: 8f1fe34e38edefba228fb9d01e1712e4c0916970
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96226688"
---
# <a name="obliviousoraclefromdeterministicstateoracle-function"></a>Obliviousoraclefromdeterministicstateoracle-Funktion

Namespace: [Microsoft. Quantum. Oracles](xref:Microsoft.Quantum.Oracles)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Kombiniert die Oracles `DeterministicStateOracle` und `ObliviousOracle` .

```qsharp
function ObliviousOracleFromDeterministicStateOracle (ancillaOracle : Microsoft.Quantum.Oracles.DeterministicStateOracle, signalOracle : Microsoft.Quantum.Oracles.ObliviousOracle) : Microsoft.Quantum.Oracles.ObliviousOracle
```


## <a name="input"></a>Eingabe

### <a name="ancillaoracle--deterministicstateoracle"></a>"ancillaoracle: [deterministicstateoracle](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle) "

Ein Status Vorbereitungs-Oracle-$A $ vom Typ, der `DeterministicStateOracle` für Register $a $ fungiert.


### <a name="signaloracle--obliviousoracle"></a>signaloracle: [obliviousoracle](xref:Microsoft.Quantum.Oracles.ObliviousOracle)

Ein Oracle-$U $ vom Typ `ObliviousOracle` , der gemeinsam für Register $a, s $, verhält.



## <a name="output--obliviousoracle"></a>Ausgabe: [obliviousoracle](xref:Microsoft.Quantum.Oracles.ObliviousOracle)

Ein Oracle-$O = UA $ vom Typ `ObliviousOracle` .

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Oracles. deterministicstateoracle](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)
- [Microsoft. Quantum. Oracles. schräviousoracle](xref:Microsoft.Quantum.Oracles.ObliviousOracle)