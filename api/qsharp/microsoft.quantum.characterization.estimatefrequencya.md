---
uid: Microsoft.Quantum.Characterization.EstimateFrequencyA
title: Estimatefrequescya-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: EstimateFrequencyA
qsharp.summary: Given a preparation that is adjointable and measurement, estimates the frequency with which that measurement succeeds (returns `Zero`) by performing a given number of trials.
ms.openlocfilehash: 88f0a237975c158bffcc015f79d2134b210ce83b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703650"
---
# <a name="estimatefrequencya-operation"></a>Estimatefrequescya-Vorgang

Namespace: [Microsoft. Quantum. Charakterisierung](xref:Microsoft.Quantum.Characterization)

Paketen [](https://nuget.org/packages/)


Bei einer Vorbereitung, bei der es sich um adjointable und Messungen handelt, schätzt die Häufigkeit, mit der diese Messung erfolgreich ist (gibt zurück `Zero` ), indem eine bestimmte Anzahl von Tests ausgeführt wird.

```qsharp
operation EstimateFrequencyA (preparation : (Qubit[] => Unit is Adj), measurement : (Qubit[] => Result), nQubits : Int, nMeasurements : Int) : Double
```


## <a name="input"></a>Eingabe

### <a name="preparation--qubit--unit-adj"></a>Vorbereitung: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ

Ein adjointable-Vorgang $P $, der einen bestimmten Status $ \rho $ für das Eingabe Register vorbereitet.


### <a name="measurement--qubit--__invalidresult__"></a>Messung: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => __ungültig <Result>__ 

Ein Vorgang $M $, der die Maßeinheit darstellt.


### <a name="nqubits--int"></a>nqubits: [int](xref:microsoft.quantum.lang-ref.int)

Die Anzahl der Qubits, die für die Vorbereitung und Messung jeweils ausgeführt werden.


### <a name="nmeasurements--int"></a>nmessungen: [int](xref:microsoft.quantum.lang-ref.int)

Gibt an, wie oft die Messung durchgeführt werden soll, um die gewünschte Häufigkeit einzuschätzen.



## <a name="output--double"></a>Ausgabe: [Double](xref:microsoft.quantum.lang-ref.double)

Eine Schätzung von $ \hat{p} $ der Häufigkeit, mit der $M (p (\ket{00 \cdots 0} \bra{00 \cdots 0})) $ zurückgibt `Zero` , wird mithilfe der unausgewogenen Binomial-Schätzung $ \hat{p} = n \_ {\uparamerow}/n \_ {\text{Measurements}} $ abgerufen, wobei $n \_ {\uparamerow} $ die Anzahl der `Zero` beobachteten Ergebnisse ist.

## <a name="remarks"></a>Hinweise

Bei adjointable-Vorgängen können bestimmte Annahmen festgelegt werden, z. b. durch das Aufrufen des Vorgangs, dass die Qubits auf genau denselben Zustand vorbereitet werden, sodass Zielcomputer einige Leistungsoptimierungen vornehmen können.