---
uid: Microsoft.Quantum.Canon.ApproximateQFT
title: Näherer Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApproximateQFT
qsharp.summary: Apply the Approximate Quantum Fourier Transform (AQFT) to a quantum register.
ms.openlocfilehash: 31fd87c0f61292142c7493cc29cad1082a9a2d67
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850323"
---
# <a name="approximateqft-operation"></a>Näherer Vorgang

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Wenden Sie die ungefähre quantfourier Transform (aqft) auf ein Quantum-Register an.

```qsharp
operation ApproximateQFT (a : Int, qs : Microsoft.Quantum.Arithmetic.BigEndian) : Unit is Adj + Ctl
```


## <a name="input"></a>Eingabe

### <a name="a--int"></a>a: [int](xref:microsoft.quantum.lang-ref.int)

Näherungs Parameter, der bestimmt, auf welcher Ebene die kontrollierten Z-Drehungen in der QFT-Verbindung gelöscht werden.

Der Näherungs Parameter a bestimmt die Bereinigungs Ebene der Z-Drehungen, d. h. a ∈ {0.. n} und alle Z-Drehungen 2D/2K, wobei k>a aus der QFT-Leitung entfernt werden. Es ist bekannt, dass für k >= Protokoll. (n) + Protokoll Taste (1/1) + 3 eine Grenze gebunden werden kann | | QFT-aqft | |<.


### <a name="qs--bigendian"></a>QS: [bigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian)

das Quantum-Register von n Qubits, auf das die ungefähre Quantum Fourier-Transformation angewendet wird.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Bemerkungen

Für aqft sind Z-Drehung-Gates im Format 2D/2K und Hadamard Gates erforderlich.

Es wird davon ausgegangen, dass die Eingabe und die Ausgabe in der Big-d-Codierung codiert werden.

## <a name="references"></a>References

- [*M. roetteler, Th. Beth*, Appl. Algebra eng. Commun. Co. 19 (3): 177-193 (2008)](http://doi.org/10.1007/s00200-008-0072-2)
- [*D. kopierungsarxiv* : quant-ph/0201067v1](https://arxiv.org/abs/quant-ph/0201067)