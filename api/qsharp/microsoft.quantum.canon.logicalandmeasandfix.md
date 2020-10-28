---
uid: Microsoft.Quantum.Canon.LogicalANDMeasAndFix
title: Logicalandmeasandfix-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: LogicalANDMeasAndFix
qsharp.summary: Computes the logical AND of multiple qubits.
ms.openlocfilehash: 86e4b9a8c6ed5f4f56db0ceefc8051d34e911c4c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704031"
---
# <a name="logicalandmeasandfix-operation"></a>Logicalandmeasandfix-Vorgang

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paketen [](https://nuget.org/packages/)


Berechnet das logische and von mehreren Qubits.

```qsharp
operation LogicalANDMeasAndFix (ctrlRegister : Qubit[], target : Qubit) : Unit
```


## <a name="input"></a>Eingabe

### <a name="ctrlregister--qubit"></a>ctrlregister: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Qubits-Eingabe für die mehrfach Eingabe und das Gate.


### <a name="target--qubit"></a>Ziel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

Ein Qubit, in dem die Ausgabe von und geschrieben wird. Dabei wird davon ausgegangen, dass Sie immer im Zustand "$ \ket $" gestartet werden {0} .



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Hinweise

Wenn `ctrlRegister` genau $2 $ Qubits hat, entspricht dies dem Vorgang, `CCNOT` aber Phase mit einer Phase $e ^ {i \ Pi/2} $ auf $ \ket {001} $ und $-e ^ {i \ Pi/2} $ auf $ \ket {101} $ und $ \ket {011} $.
Das Adjoint-Verfahren ist auch ein Measure-und Fixup-Ansatz, bei dem es sich nur um die Umkehrung des ursprünglichen Vorgangs handelt (siehe Verweise), aber weniger T-Gates verwendet werden.

## <a name="references"></a>Referenzen

- [*Craig Gidney* , 1709,06648](https://arxiv.org/abs/1709.06648)