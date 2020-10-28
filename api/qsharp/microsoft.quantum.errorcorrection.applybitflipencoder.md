---
uid: Microsoft.Quantum.ErrorCorrection.ApplyBitFlipEncoder
title: Applybitflipcoder-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: ApplyBitFlipEncoder
qsharp.summary: >-
  Private operation used to implement both the bit flip encoder and decoder.

  Note that this encoder can make use of in-place coherent recovery, in which case it will "cause" the error described by the initial state of `auxQubits`. In particular, if `auxQubits` are initially in the state $\ket{10}$, this will cause an $X_1$ error on the encoded qubit.
ms.openlocfilehash: 4d78cbb5892aabc600321185641bbf217bd4d745
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702558"
---
# <a name="applybitflipencoder-operation"></a>Applybitflipcoder-Vorgang

Namespace: [Microsoft. Quantum. errorcorrection](xref:Microsoft.Quantum.ErrorCorrection)

Paketen [](https://nuget.org/packages/)


Der private Vorgang, der verwendet wird, um den bitflip-Encoder und den Decoder zu implementieren

Beachten Sie, dass dieser Encoder eine direkte, kohärente Wiederherstellung verwenden kann. in diesem Fall wird der Fehler, der durch den ursprünglichen Zustand von beschrieben wird, "verursacht" `auxQubits` .
Insbesondere, wenn `auxQubits` sich anfänglich im Status $ \ket {10} $ befindet, führt dies zu einem $X _1 $ Error für das codierte Qubit.

```qsharp
operation ApplyBitFlipEncoder (coherentRecovery : Bool, data : Qubit[], scratch : Qubit[]) : Unit
```


## <a name="input"></a>Eingabe

### <a name="coherentrecovery--bool"></a>Coherent Recovery: [bool](xref:microsoft.quantum.lang-ref.bool)




### <a name="data--qubit"></a>Daten: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]




### <a name="scratch--qubit"></a>Scratch: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]





## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="references"></a>Referenzen

- doi: 10.1103/physreva. 85.044302