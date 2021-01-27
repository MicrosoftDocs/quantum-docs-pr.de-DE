---
uid: Microsoft.Quantum.Environment.GetQubitsAvailableToBorrow
title: Getqubitsavailabledeausleihen-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Environment
qsharp.name: GetQubitsAvailableToBorrow
qsharp.summary: Returns the number of qubits currently available to borrow.
ms.openlocfilehash: f2294fadb9c10d800b7a743fbfe0810f36f18516
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853248"
---
# <a name="getqubitsavailabletoborrow-operation"></a>Getqubitsavailabledeausleihen-Vorgang

Namespace: [Microsoft. Quantum. Environment](xref:Microsoft.Quantum.Environment)

Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Gibt die Anzahl der derzeit zur Verfügung stehenden Qubits zurück.

```qsharp
operation GetQubitsAvailableToBorrow () : Int
```


## <a name="output--int"></a>Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)

Die Anzahl der Qubits, die ausgeliehen werden könnten und nicht als Teil einer-Anweisung zugeordnet werden `borrowing` .
Wenn der verwendete Zielcomputer diese Informationen nicht bereitstellt, `-1` wird zurückgegeben.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Environment. getqubitsavailabletouse](xref:Microsoft.Quantum.Environment.GetQubitsAvailableToUse)