---
uid: Microsoft.Quantum.Diagnostics.AssertPhase
title: Assertphase-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertPhase
qsharp.summary: Asserts that the phase of an equal superposition state has the expected value.
ms.openlocfilehash: 59fa0f2f68b4de271b972aef776ee5097fd5c201
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98830078"
---
# <a name="assertphase-operation"></a>Assertphase-Vorgang

Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Bestätigt, dass die Phase eines gleich geordneten Superposition-Zustands den erwarteten Wert aufweist.

```qsharp
operation AssertPhase (expected : Double, qubit : Qubit, tolerance : Double) : Unit
```


## <a name="description"></a>Beschreibung

Dieser Vorgang bestätigt, dass die Phase $ \phi $ eines Quantum-Zustands, der als $ \bruchteil {e ^ {i t}} {\sqrt {2} } (e ^ {i\phi} \ Ket {0} + e ^ {-i\phi} \ Ket + e ^ {-i\phi} \ Ket) $ ausgedrückt werden kann, {1} für eine beliebige reale $t $ den erwarteten

## <a name="input"></a>Eingabe

### <a name="expected--double"></a>erwartet: [Double](xref:microsoft.quantum.lang-ref.double)

Der erwartete Wert von "$ \phi \in" (-\pi, \pi] $.


### <a name="qubit--qubit"></a>Qubit: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

Das Qubit, das den erwarteten Zustand speichert.


### <a name="tolerance--double"></a>Toleranz: [Double](xref:microsoft.quantum.lang-ref.double)

Absolute Toleranz für den Unterschied zwischen tatsächlichem und erwartetem Verhalten.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="example"></a>Beispiel

Der folgende Assert ist erfolgreich: `qubit` befindet sich im Zustand $ \ket{\psi} = e ^ {i 0,5} \ sqrt {1/2} \ Ket {0} + e ^ {i 0,5} \ sqrt {1/2} \ Ket {1} $;

- `AssertPhase(0.0,qubit,10e-10);`

`qubit` befindet sich im Status $ \ket{\psi} = e ^ {i 0,5} \ sqrt {1/2} \ Ket {0} + e ^ {-i 0,5} \ sqrt {1/2} \ Ket {1} $;

- `AssertPhase(0.5,qubit,10e-10);`

`qubit` befindet sich im Status $ \ket{\psi} = e ^ {-i 2.2} \ sqrt {1/2} \ Ket {0} + e ^ {i 0,2} \ sqrt {1/2} \ Ket {1} $;

- `AssertPhase(-1.2,qubit,10e-10);`