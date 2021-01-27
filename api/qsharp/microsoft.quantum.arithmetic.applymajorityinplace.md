---
uid: Microsoft.Quantum.Arithmetic.ApplyMajorityInPlace
title: Applymajorityinplace-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyMajorityInPlace
qsharp.summary: Applies the three-qubit majority operation in-place on a register of qubits.
ms.openlocfilehash: 10b512392b2098663c09b2e07a09c4025da90706
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843728"
---
# <a name="applymajorityinplace-operation"></a>Applymajorityinplace-Vorgang

Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Wendet den drei-Qubit-Mehrheits Vorgang direkt auf ein Register von Qubits an.

```qsharp
operation ApplyMajorityInPlace (output : Qubit, input : Qubit[]) : Unit is Adj + Ctl
```


## <a name="description"></a>Beschreibung

Mit diesem Vorgang wird die Mehrheits Funktion auf drei Qubits berechnet.

Wenn wir das Ausgabe-Qubit als $z $ und Eingabe-Qubits als $x $ und $y $ bezeichnen, führt der Vorgang die folgende Transformation aus: $ \ket{XYZ} \rightarrow \ket{x \oplus z} \ket{y \oplus z} \ket{\operatschmue{Maj} (x, y, z)} $.

## <a name="input"></a>Eingabe

### <a name="output--qubit"></a>Ausgabe: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

Das erste Eingabe-Qubit. Beachten Sie, dass die Ausgabe direkt berechnet und in diesem Qubit gespeichert wird.


### <a name="input--qubit"></a>Eingabe: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Zweite und dritte Eingabe-Qubits.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)

