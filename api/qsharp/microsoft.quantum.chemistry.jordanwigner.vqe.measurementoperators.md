---
uid: Microsoft.Quantum.Chemistry.JordanWigner.VQE.MeasurementOperators
title: Menrementoperators-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner.VQE
qsharp.name: MeasurementOperators
qsharp.summary: Computes all the measurement operators required to compute the expectation of a Jordan-Wigner term.
ms.openlocfilehash: 204ae621b77559a894f0bce14e494824d58e4ad6
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98835396"
---
# <a name="measurementoperators-function"></a>Menrementoperators-Funktion

Namespace: [Microsoft. Quantum. Chemistry. jordanwigner. vqe](xref:Microsoft.Quantum.Chemistry.JordanWigner.VQE)

Paket: [Microsoft. Quantum. Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)


Berechnet alle Mess Operatoren, die erforderlich sind, um die Erwartung eines Jordan-Wigner Begriffs zu berechnen.

```qsharp
function MeasurementOperators (nQubits : Int, indices : Int[], termType : Int) : Pauli[][]
```


## <a name="input"></a>Eingabe

### <a name="nqubits--int"></a>nqubits: [int](xref:microsoft.quantum.lang-ref.int)

Die Anzahl der zum Simulieren des molekularen Systems erforderlichen Qubits.


### <a name="indices--int"></a>Indizes: [int](xref:microsoft.quantum.lang-ref.int)[]

Ein Array, das die Indizes des Qubit-Felds enthält, auf den jeder Pauli-Operator angewendet wird.


### <a name="termtype--int"></a>Termtype: [int](xref:microsoft.quantum.lang-ref.int)

Der Typ des Jordan-Wigner Begriffs.



## <a name="output--pauli"></a>Ausgabe: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[] []

Ein Array von Mess Operatoren (jedes ist ein Array von Pauli).