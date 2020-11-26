---
uid: Microsoft.Quantum.MachineLearning.StateGenerator
title: Benutzerdefinierter stategenerator-Typ
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: StateGenerator
qsharp.summary: Describes an operation that prepares a given input to a sequential classifier.
ms.openlocfilehash: 5c9643f5c917ff3cb25fa8c046856b03cc287edd
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96211558"
---
# <a name="stategenerator-user-defined-type"></a>Benutzerdefinierter stategenerator-Typ

Namespace: [Microsoft. Quantum. machinelearning](xref:Microsoft.Quantum.MachineLearning)

Paket: [Microsoft. Quantum. machinelearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)


Beschreibt einen Vorgang, bei dem eine gegebene Eingabe auf einen sequenziellen Klassifizierer vorbereitet wird.

```qsharp

newtype StateGenerator = (NQubits : Int, Prepare : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Adj + Ctl));
```



## <a name="named-items"></a>Benannte Elemente

### <a name="nqubits--int"></a>Nqubits: [int](xref:microsoft.quantum.lang-ref.int)

Die Anzahl der Qubits, für die die codierte Eingabe definiert ist.
### <a name="prepare--littleendian--unit--is-adj--ctl"></a>Vorbereiten: die [littleerdian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) - => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL

Ein Vorgang, bei dem die codierte Eingabe für ein Little-in-Register-Register von `NQubits` Qubits vorbereitet wird.