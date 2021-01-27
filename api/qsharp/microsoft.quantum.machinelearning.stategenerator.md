---
uid: Microsoft.Quantum.MachineLearning.StateGenerator
title: Benutzerdefinierter stategenerator-Typ
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: StateGenerator
qsharp.summary: Describes an operation that prepares a given input to a sequential classifier.
ms.openlocfilehash: b4f6c3ca28e2976b6a0d58f4ef25ea943de9811e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854874"
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