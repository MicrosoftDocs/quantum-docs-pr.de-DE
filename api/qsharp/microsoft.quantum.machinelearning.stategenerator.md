---
uid: Microsoft.Quantum.MachineLearning.StateGenerator
title: Benutzerdefinierter stategenerator-Typ
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: StateGenerator
qsharp.summary: Describes an operation that prepares a given input to a sequential classifier.
ms.openlocfilehash: e3026dbae7209acd41924c0038a6f9b2c4b41197
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92722401"
---
# <a name="stategenerator-user-defined-type"></a>Benutzerdefinierter stategenerator-Typ

Namespace: [Microsoft. Quantum. machinelearning](xref:Microsoft.Quantum.MachineLearning)

Paketen [](https://nuget.org/packages/)


Beschreibt einen Vorgang, bei dem eine gegebene Eingabe auf einen sequenziellen Klassifizierer vorbereitet wird.

```qsharp

newtype StateGenerator = (NQubits : Int, Prepare : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Adj + Ctl));
```



## <a name="named-items"></a>Benannte Elemente

### <a name="nqubits--int"></a>Nqubits: [int](xref:microsoft.quantum.lang-ref.int)

Die Anzahl der Qubits, für die die codierte Eingabe definiert ist.
### <a name="prepare--littleendian--unit-adj--ctl"></a>Vorbereiten: [littleddian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL

Ein Vorgang, bei dem die codierte Eingabe für ein Little-in-Register-Register von `NQubits` Qubits vorbereitet wird.