---
uid: Microsoft.Quantum.ErrorCorrection.RecoverCSS
title: Wiederherstellungsvorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: RecoverCSS
qsharp.summary: Performs a single round of error correction by a quantum code described by a `CSS` type.
ms.openlocfilehash: eb01b1b9fccc19f0e3f1fd5ee596b95d0d61563f
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96200542"
---
# <a name="recovercss-operation"></a>Wiederherstellungsvorgang

Namespace: [Microsoft. Quantum. errorcorrection](xref:Microsoft.Quantum.ErrorCorrection)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Führt eine einzelne Fehlerkorrektur durch einen von einem-Typ beschriebenen quantumcode aus `CSS` .

```qsharp
operation RecoverCSS (code : Microsoft.Quantum.ErrorCorrection.CSS, fnX : Microsoft.Quantum.ErrorCorrection.RecoveryFn, fnZ : Microsoft.Quantum.ErrorCorrection.RecoveryFn, logicalRegister : Microsoft.Quantum.ErrorCorrection.LogicalRegister) : Unit
```


## <a name="input"></a>Eingabe

### <a name="code--css"></a>Code: [CSS](xref:Microsoft.Quantum.ErrorCorrection.CSS)

Ein Quantum CSS-Fehler Behebungs Code `CSS` , der als Typ verpackt ist, beschreibt die Codierung und Decodierung von Quantum-Daten und die Art und Weise, wie Fehler-Syndrome gemessen werden müssen.


### <a name="fnx--recoveryfn"></a>fnx: [Wiederherstellbarkeits-FN](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)

Ein `RecoveryFn` , der die einzelnen $X $ Error-Syndrom den `Pauli[]` Vorgängen zuordnet, die den erkannten Fehler korrigieren.


### <a name="fnz--recoveryfn"></a>fnz: [Wiederherstellbarkeits-FN](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)

Ein `RecoveryFn` , der die einzelnen $Z $ Error-Syndrom den `Pauli[]` Vorgängen zuordnet, die den erkannten Fehler korrigieren.


### <a name="logicalregister--logicalregister"></a>logicalregister: [logicalregister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)

Ein Array von Qubits, in denen der stabilikocodecode definiert ist.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. errorcorrection. CSS](xref:Microsoft.Quantum.ErrorCorrection.CSS)
- [Microsoft. Quantum. errorcorrection. wiederherstellungfn](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)
- [Microsoft. Quantum. errorcorrection. logicalregister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)