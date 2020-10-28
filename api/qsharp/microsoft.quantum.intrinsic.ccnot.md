---
uid: Microsoft.Quantum.Intrinsic.CCNOT
title: Ccnot-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: CCNOT
qsharp.summary: Applies the doubly controlled–NOT (CCNOT) gate to three qubits.
ms.openlocfilehash: bf20ff1e9d25d72e7e8e0207ab947a57dc394cf4
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702138"
---
# <a name="ccnot-operation"></a>Ccnot-Vorgang

Namespace: [Microsoft. Quantum. intrinsisch](xref:Microsoft.Quantum.Intrinsic)

Paketen [](https://nuget.org/packages/)


Wendet das (doppelt kontrollierte – not)-Gate auf drei Qubits an.

```qsharp
operation CCNOT (control1 : Qubit, control2 : Qubit, target : Qubit) : Unit
```


## <a name="input"></a>Eingabe

### <a name="control1--qubit"></a>Control1: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

Das erste Steuerelement-Qubit für das ccnot-Gate.


### <a name="control2--qubit"></a>Control2: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

Das zweite Steuerelement-Qubit für das ccnot-Gate.


### <a name="target--qubit"></a>Ziel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

Ziel-Qubit für das ccnot-Gate.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Hinweise

Äquivalent zu:

```qsharp
Controlled X([control1, control2], target);
```