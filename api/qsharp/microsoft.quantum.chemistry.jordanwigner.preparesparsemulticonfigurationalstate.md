---
uid: Microsoft.Quantum.Chemistry.JordanWigner.PrepareSparseMultiConfigurationalState
title: Preparesparser multiconfigurationalstate-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: PrepareSparseMultiConfigurationalState
qsharp.summary: Sparse multi-configurational state preparation of trial state by adding excitations to initial trial state.
ms.openlocfilehash: 1182f79a33784cdb49cb13db5cc97a0a45e59f9f
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703128"
---
# <a name="preparesparsemulticonfigurationalstate-operation"></a>Preparesparser multiconfigurationalstate-Vorgang

Namespace: [Microsoft. Quantum. Chemistry. jordanwigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)

Paketen [](https://nuget.org/packages/)


Durch das Hinzufügen von Erregung zum anfänglichen Testzustand wird der Zustand der multikonfigurationsestatusvorbereitung des Test Zustands erhöht.

```qsharp
operation PrepareSparseMultiConfigurationalState (initialStatePreparation : (Qubit[] => Unit), excitations : Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerInputState[], qubits : Qubit[]) : Unit
```


## <a name="input"></a>Eingabe

### <a name="initialstatepreparation--qubit--unit"></a>initialstatepreparation: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Einheit](xref:microsoft.quantum.lang-ref.unit) 

Einheitlich zum Vorbereiten des anfänglichen Test Zustands.


### <a name="excitations--jordanwignerinputstate"></a>Erregung: [jordanwignerinputstate](xref:Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerInputState)[]

Erregung des anfänglichen Test Zustands, der durch die Amplitude der Erregung und die Qubit-Indizes dargestellt wird, für die die Erregung durchgesetzt wird.


### <a name="qubits--qubit"></a>Qubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Qubits von hamiltonan.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)

