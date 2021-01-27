---
uid: Microsoft.Quantum.Canon.RAll0
title: RAll0-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: RAll0
qsharp.summary: >-
  Performs a phase shift operation.

  $R=\boldone-(1-e^{i \phi})\ket{0\cdots 0}\bra{0\cdots 0}$.
ms.openlocfilehash: 660e6633df6750747963d41a6ff28a4fd4b02d4e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840263"
---
# <a name="rall0-operation"></a>RAll0-Vorgang

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Führt einen Phasen Verschiebungs Vorgang aus.

$R = \boldone-(1-e ^ {i \phi}) \ket{0\cdots 0} \bra{0\cdots 0} $.

```qsharp
operation RAll0 (phase : Double, qubits : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a>Eingabe

### <a name="phase--double"></a>Phase: [Double](xref:microsoft.quantum.lang-ref.double)

Die Phase $ \phi $ wird auf den Status $ \ket{0\cdots 0} \bra{0\cdots 0} $ angewendet.


### <a name="qubits--qubit"></a>Qubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Das Register, dessen Zustand durch $R $ gedreht werden soll.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Canon. RAll1](xref:Microsoft.Quantum.Canon.RAll1)