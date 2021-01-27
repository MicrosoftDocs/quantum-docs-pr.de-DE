---
uid: Microsoft.Quantum.Synthesis.ApplyUnitary
title: Applyeinheitlicher-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: ApplyUnitary
qsharp.summary: >-
  Applies gate defined by 2^n x 2^n unitary matrix.

  Fails if matrix is not unitary, or has wrong size.
ms.openlocfilehash: 58215d3b05b8c6974e979d21a13869f27b436310
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98859215"
---
# <a name="applyunitary-operation"></a>Applyeinheitlicher-Vorgang

Namespace: [Microsoft. Quantum. Synthese](xref:Microsoft.Quantum.Synthesis)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Wendet ein Gate an, das durch die einheitliche Matrix 2 ^ n x 2 ^ n definiert wird.

Schlägt fehl, wenn die Matrix nicht einheitlich ist oder die falsche Größe aufweist.

```qsharp
operation ApplyUnitary (unitary : Microsoft.Quantum.Math.Complex[][], qubits : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="input"></a>Eingabe

### <a name="unitary--complex"></a>einheitlich: [Komplex](xref:Microsoft.Quantum.Math.Complex)[] []

2 ^ n x 2 ^ n einheitliche Matrix, die den Vorgang beschreibt.
Wenn die Matrix nicht einheitlich oder nicht von der passenden Größe ist, wird von eine Ausnahme ausgelöst.


### <a name="qubits--littleendian"></a>Qubits: [littleenddian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Die Qubits, auf die das Vorgangs Register der Länge n angewendet wird.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)

