---
uid: Microsoft.Quantum.Canon.UncurriedOpC
title: Uncurriedopc-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: UncurriedOpC
qsharp.summary: Given a function which returns operations, returns a new operation which takes both inputs as a tuple. The modifier `C` indicates that the operations are controllable.
ms.openlocfilehash: 05df99dce8b167f32078ce256748647ceb94d0fe
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98851989"
---
# <a name="uncurriedopc-function"></a>Uncurriedopc-Funktion

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Gibt eine Funktion zurück, die Vorgänge zurückgibt, gibt einen neuen Vorgang zurück, der beide Eingaben als Tupel annimmt.
Der-Modifizierer `C` gibt an, dass die Vorgänge steuerbar sind.

```qsharp
function UncurriedOpC<'T, 'U> (curriedOp : ('T -> ('U => Unit is Ctl))) : (('T, 'U) => Unit is Ctl)
```


## <a name="input"></a>Eingabe

### <a name="curriedop--t---u--unit--is-ctl"></a>curriedop: 't-> ' U => [Unit](xref:microsoft.quantum.lang-ref.unit)  ist CTL

Eine Funktion, die Vorgänge zurückgibt.



## <a name="output--tu--unit--is-ctl"></a>Ausgabe: ('t, ' U) => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist CTL

Ein neuer Vorgang `op` , der `op(t, u)` entspricht `(curriedOp(t))(u)` .

## <a name="type-parameters"></a>Typparameter

### <a name="t"></a>GIF

Der Typ des ersten Arguments einer Curry-Funktion.
### <a name="u"></a>"U

Der Typ des zweiten Arguments einer Curry-Funktion.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Canon. uncurriedop](xref:Microsoft.Quantum.Canon.UncurriedOp)