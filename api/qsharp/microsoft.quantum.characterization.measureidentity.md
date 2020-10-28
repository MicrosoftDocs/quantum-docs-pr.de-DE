---
uid: Microsoft.Quantum.Characterization.MeasureIdentity
title: Measureidentity-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: MeasureIdentity
qsharp.summary: Measures the identity operator on a register of qubits.
ms.openlocfilehash: 71a103fddb3a27703318975bea94bc7a22a9ce81
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703608"
---
# <a name="measureidentity-operation"></a>Measureidentity-Vorgang

Namespace: [Microsoft. Quantum. Charakterisierung](xref:Microsoft.Quantum.Characterization)

Paketen [](https://nuget.org/packages/)


Misst den Identitäts Operator für ein Register von Qubits.

```qsharp
operation MeasureIdentity (register : Qubit[]) : Result
```


## <a name="input"></a>Eingabe

### <a name="register--qubit"></a>Register: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Das zu messende Register.



## <a name="output--__invalidresult__"></a>Ausgabe: __ungültig <Result>__

Der Ergebniswert `Zero` .

## <a name="remarks"></a>Hinweise

Da $ \boldone $ nur den eigen Wert $1 $ und keinen negativen eigen Wert aufweist, gibt dieser Vorgang immer zurück `Zero` , was dem Eigen Wert $ + 1 = (-1) ^ 0 $ entspricht, und führt nicht zu einem zuklappen des Zustands von `register` .

Dieser Vorgang ist zwar nicht sinnvoll, aber im Kontext der Prozess Tomographie hilfreich, da er Informationen über die Beibehaltung der Ablauf Verfolgung eines Quantum-Prozesses bereitstellt.
Vor allem sollte ein Zielcomputer mit Verlust Messung diesen Vorgang durch eine tatsächliche Messung von $ \boldone $ ersetzen.