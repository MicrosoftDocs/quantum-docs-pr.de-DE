---
uid: Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerFermionImpl
title: Jordanwignerfermionimpl-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: JordanWignerFermionImpl
qsharp.summary: >-
  Represents a dynamical generator as a set of simulatable gates and an expansion in the JordanWigner basis.

  See [Dynamical Generator Modeling](../libraries/data-structures#dynamical-generator-modeling) for more details.
ms.openlocfilehash: 5b975457803b8978d846bcd3c8256dfacdb90bee
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98838182"
---
# <a name="jordanwignerfermionimpl-operation"></a>Jordanwignerfermionimpl-Vorgang

Namespace: [Microsoft. Quantum. Chemistry. jordanwigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)

Paket: [Microsoft. Quantum. Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)


Stellt einen dynamischen Generator als Satz von simulier baren Gates und eine Erweiterung in der jordanwigner-Basis dar.

Weitere Informationen finden Sie unter [Dynamical Generator Modeling](../libraries/data-structures#dynamical-generator-modeling) .

```qsharp
operation JordanWignerFermionImpl (generatorIndex : Microsoft.Quantum.Simulation.GeneratorIndex, stepSize : Double, qubits : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a>Eingabe

### <a name="generatorindex--generatorindex"></a>generatorindex: [generatorindex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)

Ein Generator Index, der als einheitliche Evolution in der jordanwigner dargestellt werden soll.


### <a name="stepsize--double"></a>stepSize: [Double](xref:microsoft.quantum.lang-ref.double)

Ein Multiplikator für die Dauer der Zeit-Evolution mit dem Begriff, auf den in verwiesen wird `generatorIndex` .


### <a name="qubits--qubit"></a>Qubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Registrieren Sie sich für den Time-Evolution-Operator.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)

