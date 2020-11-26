---
uid: Microsoft.Quantum.Canon.Compose
title: Compose-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Compose
qsharp.summary: Returns the composition of two functions.
ms.openlocfilehash: f8c6ad36220b48be1723c2d91cbf7c0a4947af14
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96216760"
---
# <a name="compose-function"></a>Compose-Funktion

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Gibt die Komposition zweier Funktionen zurück.

```qsharp
function Compose<'T, 'U, 'V> (outer : ('U -> 'V), inner : ('T -> 'U)) : ('T -> 'V)
```


## <a name="description"></a>BESCHREIBUNG

Wenn zwei Funktionen $f $ und $g $, gibt eine neue Funktion zurück, die $f \circ g $ darstellt.

## <a name="input"></a>Eingabe

### <a name="outer--u---v"></a>Outer: "U->" V

Die zweite Funktion, die angewendet werden soll.


### <a name="inner--t---u"></a>innere: 't-> ' U

Die erste Funktion, die angewendet werden soll.



## <a name="output--t---v"></a>Ausgabe: 't-> ' V

Eine neue Funktion $h $, sodass für alle Eingaben $x $, $f (g (x)) = h (x) $.

## <a name="type-parameters"></a>Typparameter

### <a name="t"></a>GIF

Der Eingabetyp der ersten Funktion, die angewendet werden soll.
### <a name="u"></a>"U

Der Ausgabetyp der ersten Funktion, die angewendet werden soll, und der Eingabetyp der zweiten Funktion, die angewendet werden soll.
### <a name="v"></a>"V

Der Ausgabetyp der zweiten Funktion, die angewendet werden soll.