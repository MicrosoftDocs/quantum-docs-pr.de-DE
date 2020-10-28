---
uid: Microsoft.Quantum.Arithmetic.FixedPoint
title: Benutzerdefinierter FixedPoint-Typ
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: FixedPoint
qsharp.summary: Represents a register of qubits encoding a fixed-point number. Consists of an integer that is equal to the number of qubits to the left of the binary point, i.e., qubits of weight greater than or equal to 1, and a quantum register.
ms.openlocfilehash: f1370cd2f8a7d6488ae0f6be841abd95e61f038e
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707295"
---
# <a name="fixedpoint-user-defined-type"></a>Benutzerdefinierter FixedPoint-Typ

Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)

Paketen [](https://nuget.org/packages/)


Stellt ein Register der Qubits-Codierung einer Festkomma Zahl dar. Besteht aus einer ganzen Zahl, die gleich der Anzahl der Qubits Links vom binären Punkt ist, d. h., Qubits mit Gewichtung größer oder gleich 1 und einem Quantum-Register.

```qsharp

newtype FixedPoint = (Int, Qubit[]);
```

