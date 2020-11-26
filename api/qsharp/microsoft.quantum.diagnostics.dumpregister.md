---
uid: Microsoft.Quantum.Diagnostics.DumpRegister
title: Dumpregiester-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: DumpRegister
qsharp.summary: Dumps the current target machine's status associated with the given qubits.
ms.openlocfilehash: 9623d6d881f1f0ec048c3a951fe259bdfac84766
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96202021"
---
# <a name="dumpregister-function"></a>Dumpregiester-Funktion

Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Sichert den aktuellen Status des Ziel Computers, der mit den angegebenen Qubits verknüpft ist.

```qsharp
function DumpRegister<'T> (location : 'T, qubits : Qubit[]) : Unit
```


## <a name="input"></a>Eingabe

### <a name="location--t"></a>Speicherort: 't

Enthält Informationen dazu, wo der Zustands Speicher generiert werden soll.


### <a name="qubits--qubit"></a>Qubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Die Liste der zu berichtenden Qubits.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)

Keine

## <a name="type-parameters"></a>Typparameter

### <a name="t"></a>GIF



## <a name="remarks"></a>Bemerkungen

Mit dieser Methode können Sie die Informationen, die dem Zustand der angegebenen Qubits zugeordnet sind, in einer Datei oder an einem anderen Speicherort speichern.
Die tatsächlich generierten Informationen und die Semantik von `location` sind für jeden Zielcomputer spezifisch. Wenn Sie jedoch ein leeres Tupel als Speicherort () bereitstellen, bedeutet dies in `()` der Regel, dass die Ausgabe in der Konsole generiert wird.

Für den lokalen vollständigen Zustands Simulator, der als Teil des Quantum Development Kit verteilt ist, erwartet diese Methode eine Zeichenfolge mit dem Pfad zu einer Datei, in der der Zustand der angegebenen Qubits (d. h. die Wave-Funktion des entsprechenden Subsystems) als eindimensionales Array komplexer Zahlen geschrieben wird, wobei jedes Element die Verstärkung der Wahrscheinlichkeit darstellt, dass der entsprechende Zustand gemessen wird.
Wenn die angegebenen Qubits mit einem anderen Qubit entkoppelt werden und ihr Zustand nicht getrennt werden kann, meldet Sie lediglich, dass die Qubits entkoppelt sind.