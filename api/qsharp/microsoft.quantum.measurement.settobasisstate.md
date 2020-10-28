---
uid: Microsoft.Quantum.Measurement.SetToBasisState
title: Setdebasisstate-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: SetToBasisState
qsharp.summary: Sets a qubit to a given computational basis state by measuring the qubit and applying a bit flip if needed.
ms.openlocfilehash: bb40ddcf6518a30f5d88eec21cf8e2c2d6e0bbaf
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92724670"
---
# <a name="settobasisstate-operation"></a>Setdebasisstate-Vorgang

Namespace: [Microsoft. Quantum. Measurement](xref:Microsoft.Quantum.Measurement)

Paketen [](https://nuget.org/packages/)


Legt ein Qubit auf einen angegebenen Berechnungsbasis Zustand fest, indem das Qubit gemessen und bei Bedarf ein bitflip angewendet wird.

```qsharp
operation SetToBasisState (desired : Result, target : Qubit) : Unit
```


## <a name="input"></a>Eingabe

### <a name="desired--__invalidresult__"></a>gewünscht: __ungültig <Result>__

Der Basiszustand, auf den das Qubit festgelegt werden soll.


### <a name="target--qubit"></a>Ziel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

Das Qubit, dessen Zustand festgelegt werden soll.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Hinweise

Als invariante dieses Vorgangs wird beim Aufrufen von `M(q)` sofort nach der Wert `SetToBasisState(result, q)` zurückgegeben `result` .