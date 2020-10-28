---
uid: Microsoft.Quantum.Canon.BoundC
title: Boundc-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: BoundC
qsharp.summary: Given an array of operations acting on a single input, produces a new operation that performs each given operation in sequence. The modifier `C` indicates that all operations in the array are controllable.
ms.openlocfilehash: 04dca4ff317bf3cee053f7c3903112f4e05a3973
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704455"
---
# <a name="boundc-function"></a>Boundc-Funktion

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paketen [](https://nuget.org/packages/)


Bei einem Array von Vorgängen, die für eine einzelne Eingabe agieren, erzeugt einen neuen Vorgang, der jeden gegebenen Vorgang nacheinander ausführt.
Der-Modifizierer `C` gibt an, dass alle Vorgänge im Array steuerbar sind.

```qsharp
function BoundC<'T> (operations : ('T => Unit is Ctl)[]) : ('T => Unit is Ctl)
```


## <a name="input"></a>Eingabe

### <a name="operations--t--unit-ctl"></a>Vorgänge: 't => [Unit](xref:microsoft.quantum.lang-ref.unit) CTL []

Eine Sequenz von Vorgängen, die für eine angegebene Eingabe ausgeführt werden soll.



## <a name="output--t--unit-ctl"></a>Ausgabe: 't => [Unit](xref:microsoft.quantum.lang-ref.unit) CTL

Ein neuer Vorgang, der jeden gegebenen Vorgang nacheinander für seine Eingabe ausführt.

## <a name="type-parameters"></a>Typparameter

### <a name="t"></a>GIF

Das Ziel, auf dem die einzelnen Vorgänge im Array agieren.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Canon. Bound](xref:Microsoft.Quantum.Canon.Bound)