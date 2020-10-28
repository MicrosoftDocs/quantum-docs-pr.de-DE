---
uid: Microsoft.Quantum.Characterization.EstimateOverlapBetweenStates
title: Estimateoverlapbetweendstates-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: EstimateOverlapBetweenStates
qsharp.summary: Given two operations which each prepare copies of a state, estimates the squared overlap between the states prepared by each operation.
ms.openlocfilehash: 58a367c7ff7d13ac5c1eb1588fb8dac66414776c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703620"
---
# <a name="estimateoverlapbetweenstates-operation"></a>Estimateoverlapbetweendstates-Vorgang

Namespace: [Microsoft. Quantum. Charakterisierung](xref:Microsoft.Quantum.Characterization)

Paketen [](https://nuget.org/packages/)


Bei zwei Vorgängen, bei denen Kopien eines Zustands vorbereitet werden, wird die Quadrat Überschneidung zwischen den von jedem Vorgang vorbereiteten Zuständen geschätzt.

```qsharp
operation EstimateOverlapBetweenStates (preparation1 : (Qubit[] => Unit is Adj), preparation2 : (Qubit[] => Unit is Adj), nQubits : Int, nMeasurements : Int) : Double
```


## <a name="input"></a>Eingabe

### <a name="preparation1--qubit--unit-adj"></a>preparation1: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ

Der erste der beiden Zustands Vorbereitungs Vorgänge, die verglichen werden sollen.


### <a name="preparation2--qubit--unit-adj"></a>preparation2: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ

Die zweite der beiden Zustands Vorbereitungs Vorgänge, die verglichen werden sollen.


### <a name="nqubits--int"></a>nqubits: [int](xref:microsoft.quantum.lang-ref.int)

Die Anzahl der Qubits, für die `commonPreparation` , `preparation1` und `preparation2` alle agieren.


### <a name="nmeasurements--int"></a>nmessungen: [int](xref:microsoft.quantum.lang-ref.int)

Die Anzahl der Messungen, die beim Schätzen der Überlappung verwendet werden sollen.



## <a name="output--double"></a>Ausgabe: [Double](xref:microsoft.quantum.lang-ref.double)



## <a name="remarks"></a>Hinweise

Bei diesem Vorgang wird der Swap-Test verwendet, um $ $ \begin{align} \left | \braket{00\cdots 0 | V ^ {\dagger} U | 00 \ cdots 0} \right | ^ 2 \end{align} $ $, wobei $U $ die einheitliche Darstellung der Aktion von `preparation1` und wobei $V $ entspricht `preparation2` .

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Charakterisierung. estimaterealoverlapbetweerstates](xref:Microsoft.Quantum.Characterization.EstimateRealOverlapBetweenStates)
- [Microsoft. Quantum. Charakteri. estimateimagoverlapbetweendstates](xref:Microsoft.Quantum.Characterization.EstimateImagOverlapBetweenStates)