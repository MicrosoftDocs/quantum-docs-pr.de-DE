---
uid: Microsoft.Quantum.Oracles.ReflectionOracleFromDeterministicStateOracle
title: Reflectionoraclefromdeterministicstateoracle-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: ReflectionOracleFromDeterministicStateOracle
qsharp.summary: Constructs reflection about a given state from an oracle.
ms.openlocfilehash: c2d37216aebcdc5243d0f1d6ec9db261cc9bd0c8
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92722178"
---
# <a name="reflectionoraclefromdeterministicstateoracle-function"></a>Reflectionoraclefromdeterministicstateoracle-Funktion

Namespace: [Microsoft. Quantum. Oracles](xref:Microsoft.Quantum.Oracles)

Paketen [](https://nuget.org/packages/)


Erstellt Reflektion über einen angegebenen Zustand aus einem Oracle.

```qsharp
function ReflectionOracleFromDeterministicStateOracle (oracle : Microsoft.Quantum.Oracles.DeterministicStateOracle) : Microsoft.Quantum.Oracles.ReflectionOracle
```


## <a name="description"></a>BESCHREIBUNG

Bei einem durch eine einheitliche Matrix $O $ dargestellten deterministischen Zustands Vorbereitungs-Oracle ist das Ergebnis dieser Funktion ein Oracle, das eine Reflektion auf den Status $ \ket{\psi} $ anwendet, der von Oracle $O $; vorbereitet wurde. Das heißt, der Status $ \ket{\psi} $, sodass $O \ket {0} = \ket{\psi} $.

## <a name="input"></a>Eingabe

### <a name="oracle--deterministicstateoracle"></a>Oracle: [deterministicstateoracle](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)

Ein Oracle, das Kopien des Zustands $ \ket{\psi} $ vorbereitet.



## <a name="output--reflectionoracle"></a>Ausgabe: [reflectionoracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)

Ein Oracle, das den Status $ \ket{\psi} $ widerspiegelt.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Oracles. deterministicstateoracle](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)
- [Microsoft. Quantum. Oracles. reflectionoracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)