---
uid: Microsoft.Quantum.Preparation._PrepareAmplitudesFromZeroState
title: _PrepareAmplitudesFromZeroState Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: _PrepareAmplitudesFromZeroState
qsharp.summary: Given a set of coefficients and a little-endian encoded quantum register of unentangled qubits, all of which are in zero state, prepares a state on that register described by the given coefficients. Uses state emulation if supported by the target.
ms.openlocfilehash: 94563632d514f66608b14c264a73bdfcc6f50982
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854457"
---
# <a name="_prepareamplitudesfromzerostate-operation"></a>_PrepareAmplitudesFromZeroState Vorgang

Namespace: [Microsoft. Quantum. Preparation](xref:Microsoft.Quantum.Preparation)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Wenn ein Satz von Koeffizienten und ein Little-Endian-codiertes Quantum-Register mit nicht entwinkeltem Qubits, die alle den Status NULL aufweisen, einen Status für das Register vorbereitet, das von den gegebenen Koeffizienten beschrieben wird. Verwendet die Zustands Emulation, wenn dies vom Ziel unterstützt wird.

```qsharp
operation _PrepareAmplitudesFromZeroState (coefficients : Microsoft.Quantum.Math.ComplexPolar[], qubits : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="input"></a>Eingabe

### <a name="coefficients--complexpolar"></a>Koeffizienten: [complexpolar](xref:Microsoft.Quantum.Math.ComplexPolar)[]




### <a name="qubits--littleendian"></a>Qubits: [littleenddian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)





## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)

