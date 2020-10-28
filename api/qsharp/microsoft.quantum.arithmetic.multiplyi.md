---
uid: Microsoft.Quantum.Arithmetic.MultiplyI
title: Multiplyi-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: MultiplyI
qsharp.summary: Multiply integer `xs` by integer `ys` and store the result in `result`, which must be zero initially.
ms.openlocfilehash: 7b44f64fdddfd95f51683c2c3b2f4d37d0cf6841
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706370"
---
# <a name="multiplyi-operation"></a>Multiplyi-Vorgang

Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)

Paketen [](https://nuget.org/packages/)


Multiplizieren Sie Integer `xs` nach Ganzzahl `ys` , und speichern Sie das Ergebnis in `result` , das anfänglich NULL sein muss.

```qsharp
operation MultiplyI (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian, result : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="input"></a>Eingabe

### <a name="xs--littleendian"></a>xs: [littleenddian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

$n $-Bit Multiplikand (littleEndian)


### <a name="ys--littleendian"></a>YS: [littleumdian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

$n $-Bit-Multiplikator (littleEndian)


### <a name="result--littleendian"></a>Ergebnis: [littleenddian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

$2N $-Bit-Ergebnis (littleEndian) muss zunächst den Status $ \ket {0} $ aufweisen.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Hinweise

Verwendet einen standardmäßigen Verschiebungs-und Add-Ansatz zum Implementieren der Multiplikation.
Die kontrollierte Version wurde verbessert, indem $x _I $ in ein von den Steuerelement-Qubits vorgelegter Ancilla-Qubit kopiert und anschließend die Addition für das Ancilla-Qubit gesteuert wurde.