---
uid: Microsoft.Quantum.Simulation.EstimateEnergyWithAdiabaticEvolution
title: Estimateenergywithadiabaticevolution-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: EstimateEnergyWithAdiabaticEvolution
qsharp.summary: Performs state preparation by applying a `statePrepUnitary` on an automatically allocated input state, followed by adiabatic state preparation using a `adiabaticUnitary`, and finally phase estimation with respect to `qpeUnitary`on the resulting state using a `phaseEstAlgorithm`.
ms.openlocfilehash: b279d35418b8f013ad0d72e9a980c9bf6ce0689a
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96225328"
---
# <a name="estimateenergywithadiabaticevolution-operation"></a>Estimateenergywithadiabaticevolution-Vorgang

Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Führt die Zustands Vorbereitung durch Anwenden eines `statePrepUnitary` auf einen automatisch zugeordneten Eingabe Zustand, gefolgt von der adiabatischen Zustands Vorbereitung mithilfe eines `adiabaticUnitary` und schließlich der Phasen Schätzung in Bezug auf `qpeUnitary` den resultierenden Zustand mithilfe von aus `phaseEstAlgorithm` .

```qsharp
operation EstimateEnergyWithAdiabaticEvolution (nQubits : Int, statePrepUnitary : (Qubit[] => Unit), adiabaticUnitary : (Qubit[] => Unit), qpeUnitary : (Qubit[] => Unit is Adj + Ctl), phaseEstAlgorithm : ((Microsoft.Quantum.Oracles.DiscreteOracle, Qubit[]) => Double)) : Double
```


## <a name="input"></a>Eingabe

### <a name="nqubits--int"></a>nqubits: [int](xref:microsoft.quantum.lang-ref.int)

Anzahl von Qubits, die für die Simulation verwendet werden.


### <a name="stateprepunitary--qubit--unit"></a>stateprepeinheitlicher: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Einheit](xref:microsoft.quantum.lang-ref.unit) 

Ein Oracle, das die Zustands Vorbereitung für den ursprünglichen Dynamical-Generator darstellt.


### <a name="adiabaticunitary--qubit--unit"></a>adiabaticeinheitlicher: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Einheit](xref:microsoft.quantum.lang-ref.unit) 

Ein Oracle, das den Adiabatic Evolution-Algorithmus darstellt, der verwendet wird, um die Sweep-bis zum Endzustand des Algorithmus zu implementieren.


### <a name="qpeunitary--qubit--unit--is-adj--ctl"></a>qpeer einheitlich: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL

Ein Oracle, das einen einheitlichen Operator $U $ darstellt, der die Entwicklung für "Time $ \delta t $" unter einem Dynamical Generator mit dem "Ground State $ \ket{\phi} $" und "Ground State Energy $E = \phi \\ , \delta t $" darstellt.


### <a name="phaseestalgorithm--discreteoraclequbit--double"></a>phaseestalgorithmus: ([diskreteoracle](xref:Microsoft.Quantum.Oracles.DiscreteOracle),[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Double](xref:microsoft.quantum.lang-ref.double) 

Ein Vorgang, der die Phasen Schätzung für einen angegebenen einheitlichen Vorgang ausführt.
Weitere Informationen finden Sie unter [iterative Phasen Schätzung](/quantum/libraries/characterization#iterative-phase-estimation) .



## <a name="output--double"></a>Ausgabe: [Double](xref:microsoft.quantum.lang-ref.double)

Eine Schätzung von $ \hat{\phi} $ der Erde State Energy $ \phi $ des durch $U $ dargestellten Generators.