---
uid: Microsoft.Quantum.Canon.ApplyQuantumFourierTransform
title: Applyquantumfouriertransform-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyQuantumFourierTransform
qsharp.summary: Performs the Quantum Fourier Transform on a quantum register containing an integer in the little-endian representation.
ms.openlocfilehash: 6d3ad9ca2e0d10c264f8020e1f34687f6cbc9f94
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96218188"
---
# <a name="applyquantumfouriertransform-operation"></a>Applyquantumfouriertransform-Vorgang

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Führt die Quantum Fourier-Transformation für ein Quantum-Register durch, das eine ganze Zahl in der Little-Endian-Darstellung enthält.

```qsharp
operation ApplyQuantumFourierTransform (qs : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="input"></a>Eingabe

### <a name="qs--littleendian"></a>QS: [Little-Dian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Das Quantum-Register, auf das die Quantum Fourier-Transformation angewendet wird.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Bemerkungen

Es wird davon ausgegangen, dass die Eingabe und die Ausgabe in Little-ercodierungscodierung vorliegen.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Canon. applyquantumfouriertransformbe](xref:Microsoft.Quantum.Canon.ApplyQuantumFourierTransformBE)