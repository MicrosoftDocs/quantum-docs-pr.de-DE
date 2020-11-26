---
uid: Microsoft.Quantum.Preparation.PrepareIdentity
title: Prepareidentity-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PrepareIdentity
qsharp.summary: >-
  Given a register, prepares that register in the maximally mixed state.

  The register is prepared in the $\boldone / 2^N$ state by applying the complete depolarizing channel to each qubit, where $N$ is the length of the register.
ms.openlocfilehash: 6e0a43e61e3c49edef94db63f07ed29132d84c83
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96210436"
---
# <a name="prepareidentity-operation"></a>Prepareidentity-Vorgang

Namespace: [Microsoft. Quantum. Preparation](xref:Microsoft.Quantum.Preparation)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Bereitet bei einem Register das registrieren im Status "maximisch" vor.

Das Register wird im Zustand $ \boldone/2 ^ N $ vorbereitet, indem der gesamte depolarisierungschannel auf die einzelnen Qubits angewendet wird, wobei $N $ die Länge des Registers ist.

```qsharp
operation PrepareIdentity (register : Qubit[]) : Unit
```


## <a name="input"></a>Eingabe

### <a name="register--qubit"></a>Register: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Ein Register, dessen Zustand in der oben beschriebenen Weise depolarisiert werden soll.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Preparation. preparesinglequbitidentity](xref:Microsoft.Quantum.Preparation.PrepareSingleQubitIdentity)