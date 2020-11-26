---
uid: Microsoft.Quantum.Environment.GetQubitsAvailableToUse
title: Getqubitsavailabletouse-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Environment
qsharp.name: GetQubitsAvailableToUse
qsharp.summary: Returns the number of qubits currently available to use.
ms.openlocfilehash: ce461b03a08b4c83b9de142c957ce5c590fe9659
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96201409"
---
# <a name="getqubitsavailabletouse-operation"></a>Getqubitsavailabletouse-Vorgang

Namespace: [Microsoft. Quantum. Environment](xref:Microsoft.Quantum.Environment)

Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Gibt die Anzahl der zurzeit verfügbaren Qubits zurück.

```qsharp
operation GetQubitsAvailableToUse () : Int
```


## <a name="output--int"></a>Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)

Die Anzahl der Qubits, die in einer-Anweisung zugeordnet werden können `using` .
Wenn der verwendete Zielcomputer diese Informationen nicht bereitstellt, `-1` wird zurückgegeben.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Environment. getqubitsavailableumausleihen](xref:Microsoft.Quantum.Environment.GetQubitsAvailableToBorrow)