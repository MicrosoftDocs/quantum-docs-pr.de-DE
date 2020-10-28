---
uid: Microsoft.Quantum.Canon.BoundA
title: Bounda-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: BoundA
qsharp.summary: Given an array of operations acting on a single input, produces a new operation that performs each given operation in sequence. The modifier `A` indicates that all operations in the array are adjointable.
ms.openlocfilehash: 40c112d0572dc4eebfc284c9ef29f43706e20c64
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704466"
---
# <a name="bounda-function"></a>Bounda-Funktion

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paketen [](https://nuget.org/packages/)


Bei einem Array von Vorgängen, die für eine einzelne Eingabe agieren, erzeugt einen neuen Vorgang, der jeden gegebenen Vorgang nacheinander ausführt.
Der-Modifizierer `A` gibt an, dass alle Vorgänge im Array adjointable sind.

```qsharp
function BoundA<'T> (operations : ('T => Unit is Adj)[]) : ('T => Unit is Adj)
```


## <a name="input"></a>Eingabe

### <a name="operations--t--unit-adj"></a>Vorgänge: 't => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ []

Eine Sequenz von Vorgängen, die für eine angegebene Eingabe ausgeführt werden soll.



## <a name="output--t--unit-adj"></a>Ausgabe: 't => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ

Ein neuer Vorgang, der jeden gegebenen Vorgang nacheinander für seine Eingabe ausführt.

## <a name="type-parameters"></a>Typparameter

### <a name="t"></a>GIF

Das Ziel, auf dem die einzelnen Vorgänge im Array agieren.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Canon. Bound](xref:Microsoft.Quantum.Canon.Bound)