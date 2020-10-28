---
uid: Microsoft.Quantum.Canon.CurriedOp
title: Curriedop-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: CurriedOp
qsharp.summary: >-
  Returns a curried version of an operation on two inputs.

  That is, given an operation with two inputs, this function applies Curry's isomorphism $f(x, y) \equiv f(x)(y)$ to return an operation of one input which returns an operation of one input.
ms.openlocfilehash: 13bc3e195d8a4ba26b726f96e4dc6b83da43c3e7
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704282"
---
# <a name="curriedop-function"></a>Curriedop-Funktion

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paketen [](https://nuget.org/packages/)


Gibt eine Curry-Version eines Vorgangs für zwei Eingaben zurück.

Bei einem Vorgang mit zwei Eingaben wendet diese Funktion z. b. die "isomorphism"-$f (x, y) \equiv f (x) (y) $ an, um einen Vorgang mit einer Eingabe zurückzugeben, der einen Vorgang mit einer Eingabe zurückgibt.

```qsharp
function CurriedOp<'T, 'U> (op : (('T, 'U) => Unit)) : ('T -> ('U => Unit))
```


## <a name="input"></a>Eingabe

### <a name="op--tu--unit"></a>OP: ('t, ' U) => [Unit](xref:microsoft.quantum.lang-ref.unit) 

Ein Vorgang, dessen Eingabe ein paar ist.



## <a name="output--t---u--unit"></a>Ausgabe: 't-> ' U => [Unit](xref:microsoft.quantum.lang-ref.unit) 

Ein Vorgang, der das erste Element eines Paars akzeptiert und einen Vorgang zurückgibt, der als Eingabe das zweite Element der ursprünglichen Vorgangs Eingabe akzeptiert.

## <a name="type-parameters"></a>Typparameter

### <a name="t"></a>GIF

Der Typ der ersten Komponente einer Funktion, die für Paare definiert ist.
### <a name="u"></a>"U

Der Typ der zweiten Komponente einer Funktion, die für Paare definiert ist.

## <a name="remarks"></a>Hinweise

Die folgenden sind gleichwertig:

```qsharp
op(x, y);

let curried = CurriedOp(op);
let partial = curried(x);
partial(y);
```