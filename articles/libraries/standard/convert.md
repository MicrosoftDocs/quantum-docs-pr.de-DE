---
title: 'Typkonvertierungen in den Q# Standard-Bibliotheken'
description: 'Erfahren Sie mehr über gängige und benutzerdefinierte Typkonvertierungs Funktionen in den Q#-Standardbibliotheken.'
author: cgranade
uid: microsoft.quantum.libraries.convert
ms.author: chgranad@microsoft.com
ms.topic: article
ms.openlocfilehash: e941d7e3d76459546861410e91a03d7315183867
ms.sourcegitcommit: 6ccea4a2006a47569c4e2c2cb37001e132f17476
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/28/2020
ms.locfileid: "77907799"
---
# <a name="type-conversions"></a>Typkonvertierungen #

Q# ist eine **stark typisierte** Sprache.
Insbesondere wird Q# nicht implizit zwischen unterschiedlichen Typen umgewandelt. Beispielsweise ist `1 + 2.0` kein gültiger Q#-Ausdruck.
Stattdessen bietet Q# eine Vielzahl von Typkonvertierungs Funktionen zum Erstellen neuer Werte eines bestimmten Typs.

<xref:microsoft.quantum.core.length> hat z. b. den Ausgabetyp `Int`, sodass die Ausgabe zuerst in eine `Double` konvertiert werden muss, bevor Sie als Teil eines Gleit Komma Ausdrucks verwendet werden kann.
Dies kann mithilfe der <xref:microsoft.quantum.convert.intasdouble>-Funktion erfolgen:

```qsharp
open Microsoft.Quantum.Convert as Convert;

function HalfLength<'T>(arr : 'T[]) : Double {
    return Convert.IntAsDouble(Length(arr)) / 2.0;
}
```

Der <xref:microsoft.quantum.convert>-Namespace stellt allgemeine Typkonvertierungs Funktionen zum Arbeiten mit den grundlegenden integrierten Typen bereit, z. b. `Int`, `Double`, `BigInt`, `Result`und `Bool`:

```qsharp
let bool = Convert.ResultAsBool(One);        // true
let big = Convert.IntAsBigInt(271);          // 271L
let indices = Convert.RangeAsIntArray(0..4); // [0, 1, 2, 3, 4]
```

Der <xref:microsoft.quantum.convert>-Namespace bietet auch einige exotischere Konvertierungen, z. b. `FunctionAsOperation`, mit denen Funktionen `'T -> 'U` in neue Vorgänge `'T => 'U`konvertiert werden.

Zum Schluss bietet die Q#-Standardbibliothek eine Reihe von benutzerdefinierten Typen, z. b. <xref:microsoft.quantum.math.complex> und <xref:microsoft.quantum.arithmetic.littleendian>.
Zusammen mit diesen Typen bietet die Standardbibliothek Funktionen wie <xref:microsoft.quantum.arithmetic.bigendianaslittleendian>:

```Q#
open Microsoft.Quantum.Arithmetic as Arithmetic;

let register = Arithmetic.BigEndian(qubits);
IncrementByInteger(Arithmetic.BigEndianAsLittleEndian(register));
```
