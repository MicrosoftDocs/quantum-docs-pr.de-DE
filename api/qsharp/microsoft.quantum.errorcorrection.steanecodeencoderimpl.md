---
uid: Microsoft.Quantum.ErrorCorrection.SteaneCodeEncoderImpl
title: Steanecodeencoderimpl-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: SteaneCodeEncoderImpl
qsharp.summary: Private operation used to implement both the Steane code encoder and decoder.
ms.openlocfilehash: 81abe75e2a315fe9a994147242f3c8c9bde586ed
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98824721"
---
# <a name="steanecodeencoderimpl-operation"></a>Steanecodeencoderimpl-Vorgang

Namespace: [Microsoft. Quantum. errorcorrection](xref:Microsoft.Quantum.ErrorCorrection)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Der private Vorgang, der verwendet wird, um sowohl den Steane-Code Encoder als auch den Decoder

```qsharp
operation SteaneCodeEncoderImpl (data : Qubit[], scratch : Qubit[]) : Unit is Adj
```


## <a name="input"></a>Eingabe

### <a name="data--qubit"></a>Daten: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

ein Array mit einem Qubit, das das Eingabe-Qubit ist.


### <a name="scratch--qubit"></a>Scratch: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

ein Array mit 6 Qubits, die Redundanz hinzufügen.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)

