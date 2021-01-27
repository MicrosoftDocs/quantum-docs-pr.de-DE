---
uid: Microsoft.Quantum.Canon.CurriedOp
title: Curriedop-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: CurriedOp
qsharp.summary: >-
  Returns a curried version of an operation on two inputs.

  That is, given an operation with two inputs, this function applies Curry's isomorphism $f(x, y) \equiv f(x)(y)$ to return an operation of one input which returns an operation of one input.
ms.openlocfilehash: f811347d65a6460690163e9df631979c906bd89f
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840770"
---
# <a name="curriedop-function"></a>Curriedop-Funktion

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


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

## <a name="remarks"></a>Bemerkungen

Die folgenden sind gleichwertig:

```qsharp
op(x, y);

let curried = CurriedOp(op);
let partial = curried(x);
partial(y);
```