---
uid: Microsoft.Quantum.Canon.BoundCA
title: Boundca-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: BoundCA
qsharp.summary: Given an array of operations acting on a single input, produces a new operation that performs each given operation in sequence. The modifier `CA` indicates that all operations in the array are adjointable and controllable.
ms.openlocfilehash: d96d33781def10940479ba2eafdcc6711a0c05a5
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704434"
---
# <a name="boundca-function"></a>Boundca-Funktion

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paketen [](https://nuget.org/packages/)


Bei einem Array von Vorgängen, die für eine einzelne Eingabe agieren, erzeugt einen neuen Vorgang, der jeden gegebenen Vorgang nacheinander ausführt.
Der-Modifizierer `CA` gibt an, dass alle Vorgänge im Array adjointable und steuerbar sind.

```qsharp
function BoundCA<'T> (operations : ('T => Unit is Adj + Ctl)[]) : ('T => Unit is Adj + Ctl)
```


## <a name="input"></a>Eingabe

### <a name="operations--t--unit-adj--ctl"></a>Vorgänge: 't => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL []

Eine Sequenz von Vorgängen, die für eine angegebene Eingabe ausgeführt werden soll.



## <a name="output--t--unit-adj--ctl"></a>Ausgabe: 't => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL

Ein neuer Vorgang, der jeden gegebenen Vorgang nacheinander für seine Eingabe ausführt.

## <a name="type-parameters"></a>Typparameter

### <a name="t"></a>GIF

Das Ziel, auf dem die einzelnen Vorgänge im Array agieren.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Canon. Bound](xref:Microsoft.Quantum.Canon.Bound)