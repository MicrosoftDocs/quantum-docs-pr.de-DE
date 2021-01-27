---
uid: Microsoft.Quantum.Characterization.EstimateRealOverlapBetweenStates
title: Estimaterealoverlapbetweendstates-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: EstimateRealOverlapBetweenStates
qsharp.summary: Given two operations which each prepare copies of a state, estimates the real part of the overlap between the states prepared by each operation.
ms.openlocfilehash: 1448e760294e958b152f4ceb3faf979441ca986d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98851850"
---
# <a name="estimaterealoverlapbetweenstates-operation"></a>Estimaterealoverlapbetweendstates-Vorgang

Namespace: [Microsoft. Quantum. Charakterisierung](xref:Microsoft.Quantum.Characterization)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Bei zwei Vorgängen, bei denen Kopien eines Zustands vorbereitet werden, wird der reelle Teil der Überschneidung zwischen den Zuständen, die von jedem Vorgang vorbereitet werden, geschätzt.

```qsharp
operation EstimateRealOverlapBetweenStates (commonPreparation : (Qubit[] => Unit is Adj), preparation1 : (Qubit[] => Unit is Adj + Ctl), preparation2 : (Qubit[] => Unit is Adj + Ctl), nQubits : Int, nMeasurements : Int) : Double
```


## <a name="input"></a>Eingabe

### <a name="commonpreparation--qubit--unit--is-adj"></a>commonpreparation: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ

Ein Vorgang, der einen festgelegten Eingabe Zustand bereitet.


### <a name="preparation1--qubit--unit--is-adj--ctl"></a>preparation1: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL

Der erste der beiden Zustands Vorbereitungs Vorgänge, die verglichen werden sollen.


### <a name="preparation2--qubit--unit--is-adj--ctl"></a>preparation2: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL

Die zweite der beiden Zustands Vorbereitungs Vorgänge, die verglichen werden sollen.


### <a name="nqubits--int"></a>nqubits: [int](xref:microsoft.quantum.lang-ref.int)

Die Anzahl der Qubits, für die `commonPreparation` , `preparation1` und `preparation2` alle agieren.


### <a name="nmeasurements--int"></a>nmessungen: [int](xref:microsoft.quantum.lang-ref.int)

Die Anzahl der Messungen, die beim Schätzen der Überlappung verwendet werden sollen.



## <a name="output--double"></a>Ausgabe: [Double](xref:microsoft.quantum.lang-ref.double)



## <a name="remarks"></a>Bemerkungen

Bei diesem Vorgang wird der Hadamard-Test verwendet, um den reellen Teil von $ $ \begin{align} \braket{\psi zu suchen. V ^ {\dagger} U | \psi} \end{align} $ $, wobei $ \ket{\psi} $ der von vorbereitete Status ist `commonPreparation` , $U $ die einheitliche Darstellung der Aktion von `preparation1` und wobei $V $ entspricht `preparation2` .

## <a name="references"></a>References

- Aharonov *et al.* [quant-ph/0511096](https://arxiv.org/abs/quant-ph/0511096).

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Charakteri. estimateimagoverlapbetweendstates](xref:Microsoft.Quantum.Characterization.EstimateImagOverlapBetweenStates)
- [Microsoft. Quantum. Charakterisierung. estimateoverlapbetweendstates](xref:Microsoft.Quantum.Characterization.EstimateOverlapBetweenStates)