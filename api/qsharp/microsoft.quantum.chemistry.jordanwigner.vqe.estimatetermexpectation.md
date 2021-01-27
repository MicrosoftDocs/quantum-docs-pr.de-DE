---
uid: Microsoft.Quantum.Chemistry.JordanWigner.VQE.EstimateTermExpectation
title: Estimatetermexpectation-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner.VQE
qsharp.name: EstimateTermExpectation
qsharp.summary: Computes the energy associated to a given Jordan-Wigner Hamiltonian term
ms.openlocfilehash: 7df4c1ea859140a669698434c6f8a786ea3bc2ea
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98835672"
---
# <a name="estimatetermexpectation-operation"></a>Estimatetermexpectation-Vorgang

Namespace: [Microsoft. Quantum. Chemistry. jordanwigner. vqe](xref:Microsoft.Quantum.Chemistry.JordanWigner.VQE)

Paket: [Microsoft. Quantum. Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)


Berechnet die Energie, die einem angegebenen Jordan-Wigner hamiltona-Begriff zugeordnet ist.

```qsharp
operation EstimateTermExpectation (inputStateUnitary : (Qubit[] => Unit is Adj), ops : Pauli[][], coeffs : Double[], nQubits : Int, nSamples : Int) : Double
```


## <a name="description"></a>Beschreibung

Mit diesem Vorgang wird der Erwartungswert geschätzt, der jedem Mess Operator zugeordnet ist, und der Wert wird mithilfe von Sampling mit dem entsprechenden Koeffizienten multipliziert.
Die Ergebnisse werden in eine Variable aggregiert, die die Energie des Jordan-Wigner Begriffs enthält.

## <a name="input"></a>Eingabe

### <a name="inputstateunitary--qubit--unit--is-adj"></a>inputstateeinheitliches: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ

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