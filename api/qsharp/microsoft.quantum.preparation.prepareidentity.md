---
uid: Microsoft.Quantum.Preparation.PrepareIdentity
title: Prepareidentity-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PrepareIdentity
qsharp.summary: >-
  Given a register, prepares that register in the maximally mixed state.

  The register is prepared in the $\boldone / 2^N$ state by applying the complete depolarizing channel to each qubit, where $N$ is the length of the register.
ms.openlocfilehash: ec7e813110ccd9e6d499fc469fa27249a182b870
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855877"
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