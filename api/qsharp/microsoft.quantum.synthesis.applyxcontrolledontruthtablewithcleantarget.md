---
uid: Microsoft.Quantum.Synthesis.ApplyXControlledOnTruthTableWithCleanTarget
title: Applyxcontrolledontruthtablewithcleantarget-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: ApplyXControlledOnTruthTableWithCleanTarget
qsharp.summary: Applies the @"microsoft.quantum.intrinsic.x" operation on `target`, if the Boolean function `func` evaluates to true for the classical assignment in `controlRegister`.
ms.openlocfilehash: 904ff7e2e7e81ee966846af120e9427f4e92301c
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96203262"
---
# <a name="applyxcontrolledontruthtablewithcleantarget-operation"></a>Applyxcontrolledontruthtablewithcleantarget-Vorgang

Namespace: [Microsoft. Quantum. Synthese](xref:Microsoft.Quantum.Synthesis)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Wendet den @"microsoft.quantum.intrinsic.x" Vorgang auf an `target` , wenn die boolesche Funktion `func` für die klassische Zuweisung in als true ausgewertet wird `controlRegister` .

```qsharp
operation ApplyXControlledOnTruthTableWithCleanTarget (func : BigInt, controlRegister : Qubit[], target : Qubit) : Unit is Adj + Ctl
```


## <a name="description"></a>BESCHREIBUNG

Mit diesem Vorgang wird ein Sonderfall von implementiert @"microsoft.quantum.synthesis.applyxcontrolledontruthtable" , bei dem das Ziel-Qubit bekanntermaßen im $ \ket {0} $-Zustand ist.

Die-Implementierung nutzt @"microsoft.quantum.intrinsic.cnot" und @"microsoft.quantum.intrinsic.r1" Gates.  Die Implementierung des Adjoint-Vorgangs ist optimiert und verwendet eine maßbasierte unberechnung.

## <a name="input"></a>Eingabe

### <a name="func--bigint"></a>Func: [bigint](xref:microsoft.quantum.lang-ref.bigint)

Boolesche Wahrheitstabelle, dargestellt als große ganze Zahl


### <a name="controlregister--qubit"></a>controlregister: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Register von Steuerungs Qubits


### <a name="target--qubit"></a>Ziel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

Ziel-Qubit (muss in $ \ket {0} $ State sein)



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Synthese. applyxcontrolledontruthtable](xref:Microsoft.Quantum.Synthesis.ApplyXControlledOnTruthTable)