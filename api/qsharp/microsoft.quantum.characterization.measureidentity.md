---
uid: Microsoft.Quantum.Characterization.MeasureIdentity
title: Measureidentity-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: MeasureIdentity
qsharp.summary: Measures the identity operator on a register of qubits.
ms.openlocfilehash: f8cf5975ac9407e8c532ace08455a41d3c08d6f0
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98851822"
---
# <a name="measureidentity-operation"></a>Measureidentity-Vorgang

Namespace: [Microsoft. Quantum. Charakterisierung](xref:Microsoft.Quantum.Characterization)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Misst den Identitäts Operator für ein Register von Qubits.

```qsharp
operation MeasureIdentity (register : Qubit[]) : Result
```


## <a name="input"></a>Eingabe

### <a name="register--qubit"></a>Register: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Das zu messende Register.



## <a name="output--__invalidresult__"></a>Ausgabe: __ungültig <Result>__

Der Ergebniswert `Zero` .

## <a name="remarks"></a>Bemerkungen

Da $ \boldone $ nur den eigen Wert $1 $ und keinen negativen eigen Wert aufweist, gibt dieser Vorgang immer zurück `Zero` , was dem Eigen Wert $ + 1 = (-1) ^ 0 $ entspricht, und führt nicht zu einem zuklappen des Zustands von `register` .

Dieser Vorgang ist zwar nicht sinnvoll, aber im Kontext der Prozess Tomographie hilfreich, da er Informationen über die Beibehaltung der Ablauf Verfolgung eines Quantum-Prozesses bereitstellt.
Vor allem sollte ein Zielcomputer mit Verlust Messung diesen Vorgang durch eine tatsächliche Messung von $ \boldone $ ersetzen.