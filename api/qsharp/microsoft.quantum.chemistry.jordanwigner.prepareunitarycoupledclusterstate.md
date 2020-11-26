---
uid: Microsoft.Quantum.Chemistry.JordanWigner.PrepareUnitaryCoupledClusterState
title: Prepareunitarycoupledclusterstate-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: PrepareUnitaryCoupledClusterState
qsharp.summary: Unitary coupled-cluster state preparation of trial state
ms.openlocfilehash: 9a2a07b1048f872ff8ff1e2dd68df73da5eb1fe0
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96224750"
---
# <a name="prepareunitarycoupledclusterstate-operation"></a>Prepareunitarycoupledclusterstate-Vorgang

Namespace: [Microsoft. Quantum. Chemistry. jordanwigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)

Paket: [Microsoft. Quantum. Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)


Einheitlicher verknüpfter Cluster Status Vorbereitung des Test Zustands

```qsharp
operation PrepareUnitaryCoupledClusterState (initialStatePreparation : (Qubit[] => Unit), clusterOperator : Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerInputState[], trotterStepSize : Double, qubits : Qubit[]) : Unit
```


## <a name="input"></a>Eingabe

### <a name="initialstatepreparation--qubit--unit"></a>initialstatepreparation: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Einheit](xref:microsoft.quantum.lang-ref.unit) 

Einheitlich zum Vorbereiten des anfänglichen Test Zustands.


### <a name="clusteroperator--jordanwignerinputstate"></a>clusteroperator: [jordanwignerinputstate](xref:Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerInputState)[]




### <a name="trotterstepsize--double"></a>trotterstepsize: [Double](xref:microsoft.quantum.lang-ref.double)




### <a name="qubits--qubit"></a>Qubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Qubits von hamiltonan.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)

