---
uid: Microsoft.Quantum.Canon.Compose
title: Compose-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Compose
qsharp.summary: Returns the composition of two functions.
ms.openlocfilehash: 02cff7eef4d55d27d5d72e6219a90b7d8f5beb3b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704354"
---
# <a name="compose-function"></a>Compose-Funktion

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paketen [](https://nuget.org/packages/)


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