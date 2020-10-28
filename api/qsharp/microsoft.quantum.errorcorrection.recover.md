---
uid: Microsoft.Quantum.ErrorCorrection.Recover
title: Wiederherstellungs Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: Recover
qsharp.summary: Performs a single round of error correction by a quantum code described by a `QECC` type.
ms.openlocfilehash: a659399f51794a4edc1d2ff43da84e46797103fb
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702426"
---
# <a name="recover-operation"></a>Wiederherstellungs Vorgang

Namespace: [Microsoft. Quantum. errorcorrection](xref:Microsoft.Quantum.ErrorCorrection)

Paketen [](https://nuget.org/packages/)


Führt eine einzelne Fehlerkorrektur durch einen von einem-Typ beschriebenen quantumcode aus `QECC` .

```qsharp
operation Recover (code : Microsoft.Quantum.ErrorCorrection.QECC, fn : Microsoft.Quantum.ErrorCorrection.RecoveryFn, logicalRegister : Microsoft.Quantum.ErrorCorrection.LogicalRegister) : Unit
```


## <a name="input"></a>Eingabe

### <a name="code--qecc"></a>Code: [qecc](xref:Microsoft.Quantum.ErrorCorrection.QECC)

Bei einem Fehler in der Quantum-Korrektur `QECC` , der als Typ verpackt wird, werden das Codieren und Decodieren von Quantum-Daten beschrieben, und es wird beschrieben, wie Fehler Syndrome gemessen werden.


### <a name="fn--recoveryfn"></a>FN: [Wiederherstellbarkeits-FN](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)

Eine `RecoveryFn` , die jedes Fehler-Syndrom den `Pauli[]` Vorgängen zuordnet, die den erkannten Fehler beheben.


### <a name="logicalregister--logicalregister"></a>logicalregister: [logicalregister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)

Ein Array von Qubits, in denen der stabilikocodecode definiert ist.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. errorcorrection. qecc](xref:Microsoft.Quantum.ErrorCorrection.QECC)
- [Microsoft. Quantum. errorcorrection. wiederherstellungfn](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)
- [Microsoft. Quantum. errorcorrection. logicalregister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)