---
uid: Microsoft.Quantum.Canon.UncurriedOpA
title: Uncurriedopa-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: UncurriedOpA
qsharp.summary: Given a function which returns operations, returns a new operation which takes both inputs as a tuple. The modifier `A` indicates that the operations are adjointable.
ms.openlocfilehash: 21df20354ad2388891f32b1bf1c7781287904983
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703716"
---
# <a name="uncurriedopa-function"></a>Uncurriedopa-Funktion

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paketen [](https://nuget.org/packages/)


Gibt eine Funktion zurück, die Vorgänge zurückgibt, gibt einen neuen Vorgang zurück, der beide Eingaben als Tupel annimmt.
Der-Modifizierer `A` gibt an, dass die Vorgänge adjointable sind.

```qsharp
function UncurriedOpA<'T, 'U> (curriedOp : ('T -> ('U => Unit is Adj))) : (('T, 'U) => Unit is Adj)
```


## <a name="input"></a>Eingabe

### <a name="curriedop--t---u--unit-adj"></a>curriedop: 't-> ' U => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ

Eine Funktion, die Vorgänge zurückgibt.



## <a name="output--tu--unit-adj"></a>Ausgabe: ('t, ' U) => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ

Ein neuer Vorgang `op` , der `op(t, u)` entspricht `(curriedOp(t))(u)` .

## <a name="type-parameters"></a>Typparameter

### <a name="t"></a>GIF

Der Typ des ersten Arguments einer Curry-Funktion.
### <a name="u"></a>"U

Der Typ des zweiten Arguments einer Curry-Funktion.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Canon. uncurriedop](xref:Microsoft.Quantum.Canon.UncurriedOp)