---
uid: Microsoft.Quantum.MachineLearning.NQubitsRequired
title: Nqubistratrequired-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: NQubitsRequired
qsharp.summary: Returns the number of qubits required to apply a given sequential classifier.
ms.openlocfilehash: e910edb9bf432e6acb5c349ee6b9d65797aaaba7
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96211660"
---
# <a name="nqubitsrequired-function"></a>Nqubistratrequired-Funktion

Namespace: [Microsoft. Quantum. machinelearning](xref:Microsoft.Quantum.MachineLearning)

Paket: [Microsoft. Quantum. machinelearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)


Gibt die Anzahl der zum Anwenden eines bestimmten sequenziellen Klassifizierers erforderlichen Qubits zurück.

```qsharp
function NQubitsRequired (model : Microsoft.Quantum.MachineLearning.SequentialModel) : Int
```


## <a name="input"></a>Eingabe

### <a name="model--sequentialmodel"></a>Modell: [sequentialmodel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)





## <a name="output--int"></a>Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)

Die Mindestgröße eines Registers, für das der sequenzielle Klassifizierer angewendet werden kann.