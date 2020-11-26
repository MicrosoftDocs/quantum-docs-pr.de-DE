---
uid: Microsoft.Quantum.Intrinsic.Reset
title: Vorgang zurücksetzen
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: Reset
qsharp.summary: Given a single qubit, measures it and ensures it is in the |0⟩ state such that it can be safely released.
ms.openlocfilehash: 61b5e4ccdf009dcb6c639e3d8e23bc73a6e475b5
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96198672"
---
# <a name="reset-operation"></a>Vorgang zurücksetzen

Namespace: [Microsoft. Quantum. intrinsisch](xref:Microsoft.Quantum.Intrinsic)

Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Wenn ein einzelnes Qubit angegeben ist, wird es gemessen und sichergestellt, dass es sich im | 0 ⟩-Zustand befindet, sodass es sicher freigegeben werden kann.

```qsharp
operation Reset (target : Qubit) : Unit
```


## <a name="input"></a>Eingabe

### <a name="target--qubit"></a>Ziel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

Das Qubit, dessen Zustand auf $ \ket $ zurückgesetzt werden soll {0} .



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)

