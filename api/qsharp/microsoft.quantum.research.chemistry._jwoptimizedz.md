---
uid: Microsoft.Quantum.Research.Chemistry._JWOptimizedZ
title: _JWOptimizedZ Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Research.Chemistry
qsharp.name: _JWOptimizedZ
qsharp.summary: Applies a Rz rotation, with a C-NOT trick to double phase in phase estimation.
ms.openlocfilehash: 76c96153b6baf8b593e0770a44b6190c075c8f53
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854232"
---
# <a name="_jwoptimizedz-operation"></a>_JWOptimizedZ Vorgang

Namespace: [Microsoft. Quantum. Research. Chemistry](xref:Microsoft.Quantum.Research.Chemistry)

Paket: [Microsoft. Quantum. Research. Chemistry](https://nuget.org/packages/Microsoft.Quantum.Research.Chemistry)


Wendet eine RZ-Drehung mit einem C-not-Trick in eine doppelte Phase in der Phasen Schätzung an.

```qsharp
operation _JWOptimizedZ (angle : Double, parityQubit : Qubit, qubit : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a>Eingabe

### <a name="angle--double"></a>Winkel: [Double](xref:microsoft.quantum.lang-ref.double)

Winkel der RZ-Drehung.


### <a name="parityqubit--qubit"></a>parameteryqubit: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

Qubit, das das Vorzeichen der Zeitentwicklung bestimmt.


### <a name="qubit--qubit"></a>Qubit: [Qubit](xref:microsoft.quantum.lang-ref.qubit)





## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)

