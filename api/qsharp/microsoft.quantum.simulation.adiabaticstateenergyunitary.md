---
uid: Microsoft.Quantum.Simulation.AdiabaticStateEnergyUnitary
title: Adiabaticstateenergyeinheitlicher-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: AdiabaticStateEnergyUnitary
qsharp.summary: Performs state preparation by applying a `statePrepUnitary` on the input state, followed by adiabatic state preparation using a `adiabaticUnitary`, and finally phase estimation with respect to `qpeUnitary`on the resulting state using a `phaseEstAlgorithm`.
ms.openlocfilehash: 642f6a0af76b3b2d0703f0377c379abf33ecee71
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92722766"
---
# <a name="adiabaticstateenergyunitary-operation"></a>Adiabaticstateenergyeinheitlicher-Vorgang

Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)

Paketen [](https://nuget.org/packages/)


Führt die Zustands Vorbereitung durch Anwenden eines `statePrepUnitary` auf den Eingabe Zustand, gefolgt von der adiabatischen Zustands Vorbereitung mithilfe eines `adiabaticUnitary` und schließlich der Phasen Schätzung in Bezug auf `qpeUnitary` den resultierenden Zustand mithilfe `phaseEstAlgorithm` von aus.

```qsharp
operation AdiabaticStateEnergyUnitary (statePrepUnitary : (Qubit[] => Unit), adiabaticUnitary : (Qubit[] => Unit), qpeUnitary : (Qubit[] => Unit is Adj + Ctl), phaseEstAlgorithm : ((Microsoft.Quantum.Oracles.DiscreteOracle, Qubit[]) => Double), qubits : Qubit[]) : Double
```


## <a name="input"></a>Eingabe

### <a name="stateprepunitary--qubit--unit"></a>stateprepeinheitlicher: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Einheit](xref:microsoft.quantum.lang-ref.unit) 

Ein Oracle, das die Zustands Vorbereitung für den ursprünglichen Dynamical-Generator darstellt.


### <a name="adiabaticunitary--qubit--unit"></a>adiabaticeinheitlicher: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Einheit](xref:microsoft.quantum.lang-ref.unit) 

Ein Oracle, das den Adiabatic Evolution-Algorithmus darstellt, der verwendet wird, um die Sweep-bis zum Endzustand des Algorithmus zu implementieren.


### <a name="qpeunitary--qubit--unit-adj--ctl"></a>qpeer einheitlich: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Einheit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL

Ein Oracle, das einen einheitlichen Operator $U $ darstellt, der die Entwicklung für "Time $ \delta t $" unter einem Dynamical Generator mit dem "Ground State $ \ket{\phi} $" und "Ground State Energy $E = \phi \\ , \delta t $" darstellt.


### <a name="phaseestalgorithm--discreteoraclequbit--double"></a>phaseestalgorithmus: ([diskreteoracle](xref:Microsoft.Quantum.Oracles.DiscreteOracle),[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Double](xref:microsoft.quantum.lang-ref.double) 

Ein Vorgang, der die Phasen Schätzung für einen angegebenen einheitlichen Vorgang ausführt.
Weitere Informationen finden Sie unter [iterative Phasen Schätzung](/quantum/libraries/characterization#iterative-phase-estimation) .


### <a name="qubits--qubit"></a>Qubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Ein Register von Qubits, das zum Ausführen der Simulation verwendet werden soll.



## <a name="output--double"></a>Ausgabe: [Double](xref:microsoft.quantum.lang-ref.double)

Eine Schätzung von $ \hat{\phi} $ der Erde State Energy $ \phi $ des durch $U $ dargestellten Generators.