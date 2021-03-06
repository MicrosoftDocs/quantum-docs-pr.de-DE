---
uid: Microsoft.Quantum.Arithmetic.FixedPoint
title: Benutzerdefinierter FixedPoint-Typ
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: FixedPoint
qsharp.summary: Represents a register of qubits encoding a fixed-point number. Consists of an integer that is equal to the number of qubits to the left of the binary point, i.e., qubits of weight greater than or equal to 1, and a quantum register.
ms.openlocfilehash: 18e85120647c5a1f41ccab5fbfb27ea602a279af
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843203"
---
# <a name="fixedpoint-user-defined-type"></a>Benutzerdefinierter FixedPoint-Typ

Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)

Paket: [Microsoft. Quantum. Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)


Stellt ein Register der Qubits-Codierung einer Festkomma Zahl dar. Besteht aus einer ganzen Zahl, die gleich der Anzahl der Qubits Links vom binären Punkt ist, d. h., Qubits mit Gewichtung größer oder gleich 1 und einem Quantum-Register.

```qsharp

newtype FixedPoint = (Int, Qubit[]);
```

