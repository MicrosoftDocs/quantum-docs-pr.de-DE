---
uid: Microsoft.Quantum.Diagnostics.DumpMachine
title: Dumpmachine-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: DumpMachine
qsharp.summary: Dumps the current target machine's status.
ms.openlocfilehash: 579300d4efb9e22cb671fbb4bce0a6f72dd0e2ca
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853422"
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

Keine.

## <a name="type-parameters"></a>Typparameter

### <a name="t"></a>GIF



## <a name="remarks"></a>Bemerkungen

Diese Methode ermöglicht es Ihnen, Informationen über den aktuellen Status des Ziel Computers in einer Datei oder an einem anderen Speicherort zu speichern.
Die tatsächlich generierten Informationen und die Semantik von `location` sind für jeden Zielcomputer spezifisch. Wenn Sie jedoch ein leeres Tupel als Speicherort ( `()` ) bereitstellen oder einfach nur den-Parameter weglassen, bedeutet dies in `location` der Regel, dass die Ausgabe in der Konsole generiert wird.

Für den lokalen vollständigen Zustands Simulator, der als Teil des Quantum Development Kit verteilt wird, erwartet diese Methode eine Zeichenfolge mit dem Pfad zu einer Datei, in der die Wave-Funktion als eindimensionales Array komplexer Zahlen geschrieben wird, wobei jedes Element die Verstärkung der Wahrscheinlichkeit darstellt, den entsprechenden Zustand zu messen.