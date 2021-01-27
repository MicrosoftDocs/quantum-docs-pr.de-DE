---
uid: Microsoft.Quantum.Measurement.MeasurePaulis
title: -Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: MeasurePaulis
qsharp.summary: Given an array of multi-qubit Pauli operators, measures each using a specified measurement gadget, then returns the array of results.
ms.openlocfilehash: 1bc14ec8e7c608d1195a03a354c71e870594f86d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853769"
---
# <a name="measurepaulis-operation"></a>-Vorgang

Namespace: [Microsoft. Quantum. Measurement](xref:Microsoft.Quantum.Measurement)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Wenn ein Array von Multi-Qubit-Pauli-Operatoren verwendet wird, werden die einzelnen Measures mit einem angegebenen Mess Gadget versehen und dann das Array der Ergebnisse zurückgegeben.

```qsharp
operation MeasurePaulis (paulis : Pauli[][], target : Qubit[], gadget : ((Pauli[], Qubit[]) => Result)) : Result[]
```


## <a name="input"></a>Eingabe

### <a name="paulis--pauli"></a>Paulis: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[] []

Array von multiqubit-Pauli-Operatoren, die gemessen werden sollen.


### <a name="target--qubit"></a>Ziel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Registrieren Sie sich, um die angegebenen Operatoren zu messen.


### <a name="gadget--pauliqubit--__invalidresult__"></a>Gadget: ([Pauli](xref:microsoft.quantum.lang-ref.pauli)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => __ungültig <Result>__ 

Der Vorgang, der die Messung eines gegebenen Multi-Qubit-Operators ausführt.



## <a name="output--__invalidresult__"></a>Ausgabe: __ungültig <Result>__[]

Das Array von Ergebnissen, das beim Messen der einzelnen Elemente von auf abgerufen wird `paulis` `target` .