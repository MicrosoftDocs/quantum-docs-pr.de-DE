---
uid: Microsoft.Quantum.ErrorCorrection.FiveQubitCodeEncoderImpl
title: Vorgang "mevequbitcodeencoderimpl"
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: FiveQubitCodeEncoderImpl
qsharp.summary: Private operation used to implement both the 5 qubit encoder and decoder.
ms.openlocfilehash: 29b0f47ddffeae3ed4dfda4084304427418e02fd
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702480"
---
# <a name="fivequbitcodeencoderimpl-operation"></a>Vorgang "mevequbitcodeencoderimpl"

Namespace: [Microsoft. Quantum. errorcorrection](xref:Microsoft.Quantum.ErrorCorrection)

Paketen [](https://nuget.org/packages/)


Privater Vorgang, der zum Implementieren des 5-Qubit-Encoders und-Decoders verwendet wird

```qsharp
operation FiveQubitCodeEncoderImpl (data : Qubit[], scratch : Qubit[]) : Unit
```


## <a name="input"></a>Eingabe

### <a name="data--qubit"></a>Daten: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

ein Array mit einem Qubit, das das Eingabe-Qubit ist.


### <a name="scratch--qubit"></a>Scratch: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

ein Array mit vier Qubits, die Redundanz hinzufügen.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Hinweise

Der ausgewählte Encoder stammt aus dem Papier V. kliuchnikov und D. Maslov, "Optimierung von Clifford-Leitungen", Phys. Rev. Phys. Rev. A 88, 052307 (2013); https://arxiv.org/abs/1305.0810, Abbildung 4B) und erfordert insgesamt 11 Gates.