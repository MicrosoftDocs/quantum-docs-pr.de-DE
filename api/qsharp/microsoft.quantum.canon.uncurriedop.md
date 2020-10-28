---
uid: Microsoft.Quantum.Canon.UncurriedOp
title: Uncurriedop-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: UncurriedOp
qsharp.summary: Given a function which returns operations, returns a new operation which takes both inputs as a tuple.
ms.openlocfilehash: 359c0b2a9dd56445fb39fadc6580809dd9fbf628
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703727"
---
# <a name="uncurriedop-function"></a>Uncurriedop-Funktion

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paketen [](https://nuget.org/packages/)


Gibt eine Funktion zurück, die Vorgänge zurückgibt, gibt einen neuen Vorgang zurück, der beide Eingaben als Tupel annimmt.

```qsharp
function UncurriedOp<'T, 'U> (curriedOp : ('T -> ('U => Unit))) : (('T, 'U) => Unit)
```


## <a name="input"></a>Eingabe

### <a name="curriedop--t---u--unit"></a>curriedop: 't-> ' U => [Unit](xref:microsoft.quantum.lang-ref.unit) 

Eine Funktion, die Vorgänge zurückgibt.



## <a name="output--tu--unit"></a>Ausgabe: ('t, ' U) => [Unit](xref:microsoft.quantum.lang-ref.unit) 

Ein neuer Vorgang `op` , der `op(t, u)` entspricht `(curriedOp(t))(u)` .

## <a name="type-parameters"></a>Typparameter

### <a name="t"></a>GIF

Der Typ der ersten Eingabe für einen geschweifenden Vorgang.
### <a name="u"></a>"U

Der Typ der zweiten Eingabe für einen geschweifenden Vorgang.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Canon. uncurriedopc](xref:Microsoft.Quantum.Canon.UncurriedOpC)
- [Microsoft. Quantum. Canon. uncurriedopa](xref:Microsoft.Quantum.Canon.UncurriedOpA)
- [Microsoft. Quantum. Canon. uncurriedopca](xref:Microsoft.Quantum.Canon.UncurriedOpCA)