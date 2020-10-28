---
uid: Microsoft.Quantum.Chemistry.JordanWigner.VQE.EstimateTermExpectation
title: Estimatetermexpectation-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner.VQE
qsharp.name: EstimateTermExpectation
qsharp.summary: Computes the energy associated to a given Jordan-Wigner Hamiltonian term
ms.openlocfilehash: ef689c55f966e63a2ab8bcdccf99d9cb5e6d3a4d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703079"
---
# <a name="estimatetermexpectation-operation"></a>Estimatetermexpectation-Vorgang

Namespace: [Microsoft. Quantum. Chemistry. jordanwigner. vqe](xref:Microsoft.Quantum.Chemistry.JordanWigner.VQE)

Paketen [](https://nuget.org/packages/)


Berechnet die Energie, die einem angegebenen Jordan-Wigner hamiltona-Begriff zugeordnet ist.

```qsharp
operation EstimateTermExpectation (inputStateUnitary : (Qubit[] => Unit is Adj), ops : Pauli[][], coeffs : Double[], nQubits : Int, nSamples : Int) : Double
```


## <a name="description"></a>BESCHREIBUNG

Mit diesem Vorgang wird der Erwartungswert geschätzt, der jedem Mess Operator zugeordnet ist, und der Wert wird mithilfe von Sampling mit dem entsprechenden Koeffizienten multipliziert.
Die Ergebnisse werden in eine Variable aggregiert, die die Energie des Jordan-Wigner Begriffs enthält.

## <a name="input"></a>Eingabe

### <a name="inputstateunitary--qubit--unit-adj"></a>inputstateeinheitliches: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ

Der für die Zustands Vorbereitung verwendete einheitliche.


### <a name="ops--pauli"></a>OPS: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[] []

Die maßoperatoren des Jordan-Wigner Begriffs.


### <a name="coeffs--double"></a>coeffs: [Double](xref:microsoft.quantum.lang-ref.double)[]

Die Koeffizienten des Jordan-Wigner Begriffs.


### <a name="nqubits--int"></a>nqubits: [int](xref:microsoft.quantum.lang-ref.int)

Die Anzahl der zum Simulieren des molekularen Systems erforderlichen Qubits.


### <a name="nsamples--int"></a>nsamples: [int](xref:microsoft.quantum.lang-ref.int)

Die Anzahl der Samplings, die für die Schätzung der Begriffs Erwartung verwendet werden sollen.



## <a name="output--double"></a>Ausgabe: [Double](xref:microsoft.quantum.lang-ref.double)

Die dem Jordan-Wigner Begriff zugeordnete Energie.