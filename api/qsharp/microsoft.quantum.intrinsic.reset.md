---
uid: Microsoft.Quantum.Intrinsic.Reset
title: Vorgang zurücksetzen
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: Reset
qsharp.summary: Given a single qubit, measures it and ensures it is in the |0⟩ state such that it can be safely released.
ms.openlocfilehash: c89cbbce49e294e56abc11b3b0492d2ed8e980a8
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707111"
---
# <a name="reset-operation"></a>Vorgang zurücksetzen

Namespace: [Microsoft. Quantum. intrinsisch](xref:Microsoft.Quantum.Intrinsic)

Paketen [](https://nuget.org/packages/)


Wenn ein einzelnes Qubit angegeben ist, wird es gemessen und sichergestellt, dass es sich im | 0 ⟩-Zustand befindet, sodass es sicher freigegeben werden kann.

```qsharp
operation Reset (target : Qubit) : Unit
```


## <a name="input"></a>Eingabe

### <a name="target--qubit"></a>Ziel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

Das Qubit, dessen Zustand auf $ \ket $ zurückgesetzt werden soll {0} .



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)

