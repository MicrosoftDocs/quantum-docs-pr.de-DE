---
uid: Microsoft.Quantum.Oracles.OracleToDiscrete
title: Oracleto Discrete-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: OracleToDiscrete
qsharp.summary: Given an operation representing a "black-box" oracle, returns a discrete-time oracle which represents the "black-box" oracle repeated multiple times.
ms.openlocfilehash: ab59cdf0ab05092a9d4e7856b7808b13df655571
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842538"
---
# <a name="oracletodiscrete-function"></a>Oracleto Discrete-Funktion

Namespace: [Microsoft. Quantum. Oracles](xref:Microsoft.Quantum.Oracles)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Bei einem Vorgang, der ein "Blackbox"-Oracle darstellt, gibt ein diskretes Oracle-Mal zurück, das den mehrfach wiederholten "Black-Box"-Oracle darstellt.

```qsharp
function OracleToDiscrete (blackBoxOracle : (Qubit[] => Unit is Adj + Ctl)) : Microsoft.Quantum.Oracles.DiscreteOracle
```


## <a name="input"></a>Eingabe

### <a name="blackboxoracle--qubit--unit--is-adj--ctl"></a>blackboxoracle: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL

Der Vorgang, der exponentiell berechnet werden soll.



## <a name="output--discreteoracle"></a>Ausgabe: [diskreteoracle](xref:Microsoft.Quantum.Oracles.DiscreteOracle)

Ein Vorgang, der teilweise über das "Blackbox"-Oracle angewendet wird, das das diskrete Zeit-Oracle darstellt.

## <a name="example"></a>Beispiel

`OracleToDiscrete(U)(3, target)` entspricht dreimal der `U(target)` Wiederholung.