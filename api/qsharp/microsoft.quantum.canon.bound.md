---
uid: Microsoft.Quantum.Canon.Bound
title: Gebundene Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Bound
qsharp.summary: Given an array of operations acting on a single input, produces a new operation that performs each given operation in sequence.
ms.openlocfilehash: c12ce37054ddde1b98778888e90916c6e4725814
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96207597"
---
# <a name="bound-function"></a>Gebundene Funktion

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Bei einem Array von Vorgängen, die für eine einzelne Eingabe agieren, erzeugt einen neuen Vorgang, der jeden gegebenen Vorgang nacheinander ausführt.

```qsharp
function Bound<'T> (operations : ('T => Unit)[]) : ('T => Unit)
```


## <a name="input"></a>Eingabe

### <a name="operations--t--unit-"></a>Vorgänge: 't => [Unit](xref:microsoft.quantum.lang-ref.unit) []

Eine Sequenz von Vorgängen, die für eine angegebene Eingabe ausgeführt werden soll.



## <a name="output--t--unit"></a>Ausgabe: 't => [Einheit](xref:microsoft.quantum.lang-ref.unit) 

Ein neuer Vorgang, der jeden gegebenen Vorgang nacheinander für seine Eingabe ausführt.

## <a name="type-parameters"></a>Typparameter

### <a name="t"></a>GIF

Das Ziel, auf dem die einzelnen Vorgänge im Array agieren.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Canon. boundc](xref:Microsoft.Quantum.Canon.BoundC)
- [Microsoft. Quantum. Canon. bounda](xref:Microsoft.Quantum.Canon.BoundA)
- [Microsoft. Quantum. Canon. boundca](xref:Microsoft.Quantum.Canon.BoundCA)