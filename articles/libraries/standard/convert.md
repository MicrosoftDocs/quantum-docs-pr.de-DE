---
title: 'Q # Standard-Bibliotheken: Typkonvertierungen | Microsoft-Dokumentation'
description: 'F #-Standardbibliotheken: Typkonvertierungen'
author: cgranade
uid: microsoft.quantum.libraries.convert
ms.author: chgranad@microsoft.com
ms.topic: article
ms.openlocfilehash: 4716f0d9562229f08ef6f0f5f80961f793de4c5c
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2019
ms.locfileid: "73184473"
---
# <a name="type-conversions"></a>Typkonvertierungen #

F # ist eine **stark typisierte** Sprache.
Insbesondere wird Q # nicht implizit zwischen unterschiedlichen Typen umgewandelt. Beispielsweise ist `1 + 2.0` kein gültiger Q #-Ausdruck.
Stattdessen bietet Q # eine Vielzahl von Typkonvertierungs Funktionen zum Erstellen neuer Werte eines bestimmten Typs.

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

Zum Schluss bietet die Q #-Standardbibliothek eine Reihe von benutzerdefinierten Typen, z. b. <xref:microsoft.quantum.math.complex> und <xref:microsoft.quantum.arithmetic.littleendian>.
Zusammen mit diesen Typen bietet die Standardbibliothek Funktionen wie <xref:microsoft.quantum.arithmetic.bigendianaslittleendian>:

```Q#
open Microsoft.Quantum.Arithmetic as Arithmetic;

let register = Arithmetic.BigEndian(qubits);
IncrementByInteger(Arithmetic.BigEndianAsLittleEndian(register));
```
