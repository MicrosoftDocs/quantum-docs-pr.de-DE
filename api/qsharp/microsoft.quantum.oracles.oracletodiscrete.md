---
uid: Microsoft.Quantum.Oracles.OracleToDiscrete
title: Oracleto Discrete-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: OracleToDiscrete
qsharp.summary: Given an operation representing a "black-box" oracle, returns a discrete-time oracle which represents the "black-box" oracle repeated multiple times.
ms.openlocfilehash: d26d57c587f24e7f74102c12753bcddb00fd8a9d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92724249"
---
# <a name="oracletodiscrete-function"></a>Oracleto Discrete-Funktion

Namespace: [Microsoft. Quantum. Oracles](xref:Microsoft.Quantum.Oracles)

Paketen [](https://nuget.org/packages/)


Bei einem Vorgang, der ein "Blackbox"-Oracle darstellt, gibt ein diskretes Oracle-Mal zurück, das den mehrfach wiederholten "Black-Box"-Oracle darstellt.

```qsharp
function OracleToDiscrete (blackBoxOracle : (Qubit[] => Unit is Adj + Ctl)) : Microsoft.Quantum.Oracles.DiscreteOracle
```


## <a name="input"></a>Eingabe

### <a name="blackboxoracle--qubit--unit-adj--ctl"></a>blackboxoracle: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL

Der Vorgang, der exponentiell berechnet werden soll.



## <a name="output--discreteoracle"></a>Ausgabe: [diskreteoracle](xref:Microsoft.Quantum.Oracles.DiscreteOracle)

Ein Vorgang, der teilweise über das "Blackbox"-Oracle angewendet wird, das das diskrete Zeit-Oracle darstellt.