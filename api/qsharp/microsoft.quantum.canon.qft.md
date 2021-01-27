---
uid: Microsoft.Quantum.Canon.QFT
title: QFT-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: QFT
qsharp.summary: Performs the Quantum Fourier Transform on a quantum register containing an integer in the big-endian representation.
ms.openlocfilehash: 30f475c3850c248b5af58db1e4aac3638c4c0471
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98852298"
---
# <a name="qft-operation"></a>QFT-Vorgang

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Führt die Quantum Fourier-Transformation für ein Quantum-Register durch, das eine ganze Zahl in der Big-Endian-Darstellung enthält.

```qsharp
operation QFT (qs : Microsoft.Quantum.Arithmetic.BigEndian) : Unit is Adj + Ctl
```


## <a name="input"></a>Eingabe

### <a name="qs--bigendian"></a>QS: [bigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian)

Das Quantum-Register, auf das die Quantum Fourier-Transformation angewendet wird.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Bemerkungen

Es wird davon ausgegangen, dass die Eingabe und die Ausgabe in der Big-d-Codierung vorliegen.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Canon. applyquantumfouriertransformbe](xref:Microsoft.Quantum.Canon.ApplyQuantumFourierTransformBE)