---
uid: Microsoft.Quantum.Canon.UncurriedOpCA
title: Uncurriedopca-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: UncurriedOpCA
qsharp.summary: Given a function which returns operations, returns a new operation which takes both inputs as a tuple. The modifier `CA` indicates that the operations are controllable and adjointable.
ms.openlocfilehash: 6a0f2e1b345d0ba3ac5c779c5dc2bfffaf659a0b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703710"
---
# <a name="uncurriedopca-function"></a>Uncurriedopca-Funktion

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paketen [](https://nuget.org/packages/)


Gibt eine Funktion zurück, die Vorgänge zurückgibt, gibt einen neuen Vorgang zurück, der beide Eingaben als Tupel annimmt.
Der-Modifizierer `CA` gibt an, dass die Vorgänge steuerbar und adjointable sind.

```qsharp
function UncurriedOpCA<'T, 'U> (curriedOp : ('T -> ('U => Unit is Ctl + Adj))) : (('T, 'U) => Unit is Ctl + Adj)
```


## <a name="input"></a>Eingabe

### <a name="curriedop--t---u--unit-ctl--adj"></a>curriedop: 't-> ' U => [Unit](xref:microsoft.quantum.lang-ref.unit) CTL + ADJ

Eine Funktion, die Vorgänge zurückgibt.



## <a name="output--tu--unit-ctl--adj"></a>Ausgabe: ('t, ' U) => [Unit](xref:microsoft.quantum.lang-ref.unit) CTL + ADJ

Ein neuer Vorgang `op` , der `op(t, u)` entspricht `(curriedOp(t))(u)` .

## <a name="type-parameters"></a>Typparameter

### <a name="t"></a>GIF

Der Typ des ersten Arguments einer Curry-Funktion.
### <a name="u"></a>"U

Der Typ des zweiten Arguments einer Curry-Funktion.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Canon. uncurriedop](xref:Microsoft.Quantum.Canon.UncurriedOp)