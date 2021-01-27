---
uid: Microsoft.Quantum.ErrorCorrection.ApplyBitFlipEncoder
title: Applybitflipcoder-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: ApplyBitFlipEncoder
qsharp.summary: >-
  Private operation used to implement both the bit flip encoder and decoder.

  Note that this encoder can make use of in-place coherent recovery, in which case it will "cause" the error described by the initial state of `auxQubits`. In particular, if `auxQubits` are initially in the state $\ket{10}$, this will cause an $X_1$ error on the encoded qubit.
ms.openlocfilehash: cc70cc409cb472a747899838d3a9ad2d78f6b5ab
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98827691"
---
# <a name="applybitflipencoder-operation"></a>Applybitflipcoder-Vorgang

Namespace: [Microsoft. Quantum. errorcorrection](xref:Microsoft.Quantum.ErrorCorrection)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Der private Vorgang, der verwendet wird, um den bitflip-Encoder und den Decoder zu implementieren

Beachten Sie, dass dieser Encoder eine direkte, kohärente Wiederherstellung verwenden kann. in diesem Fall wird der Fehler, der durch den ursprünglichen Zustand von beschrieben wird, "verursacht" `auxQubits` .
Insbesondere, wenn `auxQubits` sich anfänglich im Status $ \ket {10} $ befindet, führt dies zu einem $X _1 $ Error für das codierte Qubit.

```qsharp
operation ApplyBitFlipEncoder (coherentRecovery : Bool, data : Qubit[], scratch : Qubit[]) : Unit is Adj
```


## <a name="input"></a>Eingabe

### <a name="coherentrecovery--bool"></a>Coherent Recovery: [bool](xref:microsoft.quantum.lang-ref.bool)




### <a name="data--qubit"></a>Daten: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]




### <a name="scratch--qubit"></a>Scratch: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]





## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="references"></a>References

- doi: 10.1103/physreva. 85.044302