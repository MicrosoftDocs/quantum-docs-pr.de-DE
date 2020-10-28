---
uid: Microsoft.Quantum.Diagnostics.AssertPhase
title: Assertphase-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertPhase
qsharp.summary: Asserts that the phase of an equal superposition state has the expected value.
ms.openlocfilehash: e042c03d2a72d9ce4816a8cdb56603e175b22807
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702744"
---
# <a name="assertphase-operation"></a>Assertphase-Vorgang

Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Paketen [](https://nuget.org/packages/)


Bestätigt, dass die Phase eines gleich geordneten Superposition-Zustands den erwarteten Wert aufweist.

```qsharp
operation AssertPhase (expected : Double, qubit : Qubit, tolerance : Double) : Unit
```


## <a name="description"></a>BESCHREIBUNG

Dieser Vorgang bestätigt, dass die Phase $ \phi $ eines Quantum-Zustands, der als $ \bruchteil {e ^ {i t}} {\sqrt {2} } (e ^ {i\phi} \ Ket {0} + e ^ {-i\phi} \ Ket + e ^ {-i\phi} \ Ket) $ ausgedrückt werden kann, {1} für eine beliebige reale $t $ den erwarteten

## <a name="input"></a>Eingabe

### <a name="expected--double"></a>erwartet: [Double](xref:microsoft.quantum.lang-ref.double)

Der erwartete Wert von "$ \phi \in" (-\pi, \pi] $.


### <a name="qubit--qubit"></a>Qubit: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

Das Qubit, das den erwarteten Zustand speichert.


### <a name="tolerance--double"></a>Toleranz: [Double](xref:microsoft.quantum.lang-ref.double)

Absolute Toleranz für den Unterschied zwischen tatsächlichem und erwartetem Verhalten.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)

