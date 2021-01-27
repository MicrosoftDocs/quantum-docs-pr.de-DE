---
uid: Microsoft.Quantum.Canon.Compose
title: Compose-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Compose
qsharp.summary: Returns the composition of two functions.
ms.openlocfilehash: 73eab66e2e9a9af56d01db927eb7af38bb56a23e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840910"
---
# <a name="compose-function"></a>Compose-Funktion

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Gibt die Komposition zweier Funktionen zurück.

```qsharp
function Compose<'T, 'U, 'V> (outer : ('U -> 'V), inner : ('T -> 'U)) : ('T -> 'V)
```


## <a name="description"></a>Beschreibung

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