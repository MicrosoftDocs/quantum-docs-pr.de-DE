---
uid: Microsoft.Quantum.ErrorCorrection.SteaneCodeEncoderImpl
title: Steanecodeencoderimpl-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: SteaneCodeEncoderImpl
qsharp.summary: Private operation used to implement both the Steane code encoder and decoder.
ms.openlocfilehash: 3a9a1b11ed9255f18135e3717de7e9e1ec891298
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96200424"
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

