---
uid: Microsoft.Quantum.Canon.ApplyQuantumFourierTransform
title: Applyquantumfouriertransform-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyQuantumFourierTransform
qsharp.summary: Performs the Quantum Fourier Transform on a quantum register containing an integer in the little-endian representation.
ms.openlocfilehash: fa8d135c0665f0a576229797d208b321ba0329a6
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705098"
---
# <a name="applyquantumfouriertransform-operation"></a>Applyquantumfouriertransform-Vorgang

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paketen [](https://nuget.org/packages/)


Führt die Quantum Fourier-Transformation für ein Quantum-Register durch, das eine ganze Zahl in der Little-Endian-Darstellung enthält.

```qsharp
operation ApplyQuantumFourierTransform (qs : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="input"></a>Eingabe

### <a name="qs--littleendian"></a>QS: [Little-Dian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Das Quantum-Register, auf das die Quantum Fourier-Transformation angewendet wird.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Hinweise

Es wird davon ausgegangen, dass die Eingabe und die Ausgabe in Little-ercodierungscodierung vorliegen.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Canon. applyquantumfouriertransformbe](xref:Microsoft.Quantum.Canon.ApplyQuantumFourierTransformBE)