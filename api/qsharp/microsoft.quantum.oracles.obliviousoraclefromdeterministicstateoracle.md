---
uid: Microsoft.Quantum.Oracles.ObliviousOracleFromDeterministicStateOracle
title: Obliviousoraclefromdeterministicstateoracle-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: ObliviousOracleFromDeterministicStateOracle
qsharp.summary: Combines the oracles `DeterministicStateOracle` and `ObliviousOracle`.
ms.openlocfilehash: c7aa80feda67d68216f318073ee8c6a5eb0653c0
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854525"
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