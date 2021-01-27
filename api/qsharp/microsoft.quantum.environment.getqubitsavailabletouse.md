---
uid: Microsoft.Quantum.Environment.GetQubitsAvailableToUse
title: Getqubitsavailabletouse-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Environment
qsharp.name: GetQubitsAvailableToUse
qsharp.summary: Returns the number of qubits currently available to use.
ms.openlocfilehash: 2ed8c3789331a15b351769be960d06f6364d8047
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98827799"
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