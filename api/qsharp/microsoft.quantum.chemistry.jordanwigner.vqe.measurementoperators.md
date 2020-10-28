---
uid: Microsoft.Quantum.Chemistry.JordanWigner.VQE.MeasurementOperators
title: Menrementoperators-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner.VQE
qsharp.name: MeasurementOperators
qsharp.summary: Computes all the measurement operators required to compute the expectation of a Jordan-Wigner term.
ms.openlocfilehash: 24d752c4f198764b6e7c6ea6c49669c020c1a502
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703056"
---
# <a name="measurementoperators-function"></a>Menrementoperators-Funktion

Namespace: [Microsoft. Quantum. Chemistry. jordanwigner. vqe](xref:Microsoft.Quantum.Chemistry.JordanWigner.VQE)

Paketen [](https://nuget.org/packages/)


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