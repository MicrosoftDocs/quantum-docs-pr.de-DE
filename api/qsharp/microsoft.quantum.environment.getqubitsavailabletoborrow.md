---
uid: Microsoft.Quantum.Environment.GetQubitsAvailableToBorrow
title: Getqubitsavailabledeausleihen-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Environment
qsharp.name: GetQubitsAvailableToBorrow
qsharp.summary: Returns the number of qubits currently available to borrow. This includes unused qubits; that is, this includes the qubits returned by `GetQubitsAvailableToUse`.
ms.openlocfilehash: cb56ce4aefd7a03c0f0827b8d34688ef17988f56
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702588"
---
# <a name="getqubitsavailabletoborrow-operation"></a>Getqubitsavailabledeausleihen-Vorgang

Namespace: [Microsoft. Quantum. Environment](xref:Microsoft.Quantum.Environment)

Paketen [](https://nuget.org/packages/)


Gibt die Anzahl der derzeit zur Verfügung stehenden Qubits zurück.
Dies schließt nicht verwendete Qubits ein. Das heißt, dies schließt die von zurückgegebenen Qubits ein `GetQubitsAvailableToUse` .

```qsharp
operation GetQubitsAvailableToBorrow () : Int
```


## <a name="output--int"></a>Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)

Die Anzahl der Qubits, die in einer-Anweisung zugeordnet werden können `borrowing` .
Wenn der verwendete Zielcomputer diese Informationen nicht bereitstellt, `-1` wird zurückgegeben.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Environment. getqubitsavailabletouse](xref:Microsoft.Quantum.Environment.GetQubitsAvailableToUse)