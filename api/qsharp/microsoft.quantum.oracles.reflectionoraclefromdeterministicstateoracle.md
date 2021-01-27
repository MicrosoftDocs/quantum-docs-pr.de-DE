---
uid: Microsoft.Quantum.Oracles.ReflectionOracleFromDeterministicStateOracle
title: Reflectionoraclefromdeterministicstateoracle-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: ReflectionOracleFromDeterministicStateOracle
qsharp.summary: Constructs reflection about a given state from an oracle.
ms.openlocfilehash: c260bdbcdb2ce53ad602bf84e0d31ef4fec24a79
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842528"
---
# <a name="reflectionoraclefromdeterministicstateoracle-function"></a>Reflectionoraclefromdeterministicstateoracle-Funktion

Namespace: [Microsoft. Quantum. Oracles](xref:Microsoft.Quantum.Oracles)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Erstellt Reflektion über einen angegebenen Zustand aus einem Oracle.

```qsharp
function ReflectionOracleFromDeterministicStateOracle (oracle : Microsoft.Quantum.Oracles.DeterministicStateOracle) : Microsoft.Quantum.Oracles.ReflectionOracle
```


## <a name="description"></a>Beschreibung

Bei einem durch eine einheitliche Matrix $O $ dargestellten deterministischen Zustands Vorbereitungs-Oracle ist das Ergebnis dieser Funktion ein Oracle, das eine Reflektion auf den Status $ \ket{\psi} $ anwendet, der von Oracle $O $; vorbereitet wurde. Das heißt, der Status $ \ket{\psi} $, sodass $O \ket {0} = \ket{\psi} $.

## <a name="input"></a>Eingabe

### <a name="oracle--deterministicstateoracle"></a>Oracle: [deterministicstateoracle](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)

Ein Oracle, das Kopien des Zustands $ \ket{\psi} $ vorbereitet.



## <a name="output--reflectionoracle"></a>Ausgabe: [reflectionoracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)

Ein Oracle, das den Status $ \ket{\psi} $ widerspiegelt.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Oracles. deterministicstateoracle](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)
- [Microsoft. Quantum. Oracles. reflectionoracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)