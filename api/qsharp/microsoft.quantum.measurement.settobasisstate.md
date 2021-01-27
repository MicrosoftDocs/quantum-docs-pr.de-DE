---
uid: Microsoft.Quantum.Measurement.SetToBasisState
title: Setdebasisstate-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: SetToBasisState
qsharp.summary: Sets a qubit to a given computational basis state by measuring the qubit and applying a bit flip if needed.
ms.openlocfilehash: dfa054360a5e82b7ae6ec5a6d52e7d5fe566f42e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854622"
---
# <a name="settobasisstate-operation"></a>Setdebasisstate-Vorgang

Namespace: [Microsoft. Quantum. Measurement](xref:Microsoft.Quantum.Measurement)

Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


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



## <a name="remarks"></a>Bemerkungen

Als invariante dieses Vorgangs wird beim Aufrufen von `M(q)` sofort nach der Wert `SetToBasisState(result, q)` zurückgegeben `result` .