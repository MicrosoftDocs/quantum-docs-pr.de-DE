---
uid: Microsoft.Quantum.Canon.UncurriedOpCA
title: Uncurriedopca-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: UncurriedOpCA
qsharp.summary: Given a function which returns operations, returns a new operation which takes both inputs as a tuple. The modifier `CA` indicates that the operations are controllable and adjointable.
ms.openlocfilehash: 910d8a3006a2f217888b791e479e10f9f1a6965e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840039"
---
# <a name="uncurriedopca-function"></a>Uncurriedopca-Funktion

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Gibt eine Funktion zurück, die Vorgänge zurückgibt, gibt einen neuen Vorgang zurück, der beide Eingaben als Tupel annimmt.
Der-Modifizierer `CA` gibt an, dass die Vorgänge steuerbar und adjointable sind.

```qsharp
function UncurriedOpCA<'T, 'U> (curriedOp : ('T -> ('U => Unit is Ctl + Adj))) : (('T, 'U) => Unit is Ctl + Adj)
```


## <a name="input"></a>Eingabe

### <a name="curriedop--t---u--unit--is-adj--ctl"></a>curriedop: 't-> ' U => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL

Eine Funktion, die Vorgänge zurückgibt.



## <a name="output--tu--unit--is-adj--ctl"></a>Ausgabe: ('t, ' U) => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL

Ein neuer Vorgang `op` , der `op(t, u)` entspricht `(curriedOp(t))(u)` .

## <a name="type-parameters"></a>Typparameter

### <a name="t"></a>GIF

Der Typ des ersten Arguments einer Curry-Funktion.
### <a name="u"></a>"U

Der Typ des zweiten Arguments einer Curry-Funktion.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Canon. uncurriedop](xref:Microsoft.Quantum.Canon.UncurriedOp)