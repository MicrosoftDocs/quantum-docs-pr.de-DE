---
uid: Microsoft.Quantum.Canon.UncurriedOpC
title: Uncurriedopc-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: UncurriedOpC
qsharp.summary: Given a function which returns operations, returns a new operation which takes both inputs as a tuple. The modifier `C` indicates that the operations are controllable.
ms.openlocfilehash: f3e5ecf3f7df0393dfbb948f064c27505f04cfcf
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703715"
---
# <a name="uncurriedopc-function"></a>Uncurriedopc-Funktion

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paketen [](https://nuget.org/packages/)


Gibt eine Funktion zurück, die Vorgänge zurückgibt, gibt einen neuen Vorgang zurück, der beide Eingaben als Tupel annimmt.
Der-Modifizierer `C` gibt an, dass die Vorgänge steuerbar sind.

```qsharp
function UncurriedOpC<'T, 'U> (curriedOp : ('T -> ('U => Unit is Ctl))) : (('T, 'U) => Unit is Ctl)
```


## <a name="input"></a>Eingabe

### <a name="curriedop--t---u--unit-ctl"></a>curriedop: 't-> ' U => [Unit](xref:microsoft.quantum.lang-ref.unit) CTL

Eine Funktion, die Vorgänge zurückgibt.



## <a name="output--tu--unit-ctl"></a>Ausgabe: ('t, ' U) => [Unit](xref:microsoft.quantum.lang-ref.unit) CTL

Ein neuer Vorgang `op` , der `op(t, u)` entspricht `(curriedOp(t))(u)` .

## <a name="type-parameters"></a>Typparameter

### <a name="t"></a>GIF

Der Typ des ersten Arguments einer Curry-Funktion.
### <a name="u"></a>"U

Der Typ des zweiten Arguments einer Curry-Funktion.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Canon. uncurriedop](xref:Microsoft.Quantum.Canon.UncurriedOp)