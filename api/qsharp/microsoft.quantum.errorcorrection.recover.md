---
uid: Microsoft.Quantum.ErrorCorrection.Recover
title: Wiederherstellungs Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: Recover
qsharp.summary: Performs a single round of error correction by a quantum code described by a `QECC` type.
ms.openlocfilehash: 3e2ce404ae3a6b4097897b859388fea3f915232c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98825522"
---
# <a name="recover-operation"></a>Wiederherstellungs Vorgang

Namespace: [Microsoft. Quantum. errorcorrection](xref:Microsoft.Quantum.ErrorCorrection)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


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