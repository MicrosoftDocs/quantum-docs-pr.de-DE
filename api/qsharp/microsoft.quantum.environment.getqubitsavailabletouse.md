---
uid: Microsoft.Quantum.Environment.GetQubitsAvailableToUse
title: Getqubitsavailabletouse-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Environment
qsharp.name: GetQubitsAvailableToUse
qsharp.summary: Returns the number of qubits currently available to use.
ms.openlocfilehash: 25d43d369193fc7453fd5ce9c50769c438a69afb
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702587"
---
# <a name="getqubitsavailabletouse-operation"></a>Getqubitsavailabletouse-Vorgang

Namespace: [Microsoft. Quantum. Environment](xref:Microsoft.Quantum.Environment)

Paketen [](https://nuget.org/packages/)


Gibt die Anzahl der zurzeit verfügbaren Qubits zurück.

```qsharp
operation GetQubitsAvailableToUse () : Int
```


## <a name="output--int"></a>Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)

Die Anzahl der Qubits, die in einer-Anweisung zugeordnet werden können `using` .
Wenn der verwendete Zielcomputer diese Informationen nicht bereitstellt, `-1` wird zurückgegeben.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Environment. getqubitsavailableumausleihen](xref:Microsoft.Quantum.Environment.GetQubitsAvailableToBorrow)