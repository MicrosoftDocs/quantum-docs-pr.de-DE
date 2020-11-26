---
uid: Microsoft.Quantum.Diagnostics.DumpMachine
title: Dumpmachine-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: DumpMachine
qsharp.summary: Dumps the current target machine's status.
ms.openlocfilehash: e7eb2dfce060b61e27deae31e3c1fc6dc3d7655c
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96202106"
---
# <a name="dumpmachine-function"></a>Dumpmachine-Funktion

Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Sichert den Status des aktuellen Ziel Computers.

```qsharp
function DumpMachine<'T> (location : 'T) : Unit
```


## <a name="input"></a>Eingabe

### <a name="location--t"></a>Speicherort: 't

Stellt Informationen dazu bereit, wo das Abbild des Computers generiert werden soll.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)

Keine

## <a name="type-parameters"></a>Typparameter

### <a name="t"></a>GIF



## <a name="remarks"></a>Bemerkungen

Diese Methode ermöglicht es Ihnen, Informationen über den aktuellen Status des Ziel Computers in einer Datei oder an einem anderen Speicherort zu speichern.
Die tatsächlich generierten Informationen und die Semantik von `location` sind für jeden Zielcomputer spezifisch. Wenn Sie jedoch ein leeres Tupel als Speicherort ( `()` ) bereitstellen oder einfach nur den-Parameter weglassen, bedeutet dies in `location` der Regel, dass die Ausgabe in der Konsole generiert wird.

Für den lokalen vollständigen Zustands Simulator, der als Teil des Quantum Development Kit verteilt wird, erwartet diese Methode eine Zeichenfolge mit dem Pfad zu einer Datei, in der die Wave-Funktion als eindimensionales Array komplexer Zahlen geschrieben wird, wobei jedes Element die Verstärkung der Wahrscheinlichkeit darstellt, den entsprechenden Zustand zu messen.