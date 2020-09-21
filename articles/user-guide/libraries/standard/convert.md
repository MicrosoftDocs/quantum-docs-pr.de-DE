---
title: Typkonvertierungen in den Q# Standardbibliotheken
description: Erfahren Sie mehr über gängige und benutzerdefinierte Typkonvertierungs Funktionen in den Q# Standardbibliotheken.
author: cgranade
uid: microsoft.quantum.libraries.convert
ms.author: chgranad
ms.topic: article
no-loc:
- Q#
- $$v
ms.openlocfilehash: aa8a1ad624067906998d2735c7a95174a163ce97
ms.sourcegitcommit: 9b0d1ffc8752334bd6145457a826505cc31fa27a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/21/2020
ms.locfileid: "90835603"
---
# <a name="type-conversions"></a>Typkonvertierungen #

Q# ist eine **stark typisierte** Sprache.
Insbesondere wird Q# nicht implizit zwischen unterschiedlichen Typen umgewandelt. Beispielsweise `1 + 2.0` ist kein gültiger Q# Ausdruck.
Stattdessen Q# stellt eine Reihe von Typkonvertierungs Funktionen zum Erstellen neuer Werte eines angegebenen Typs bereit.

Hat z. b. <xref:microsoft.quantum.core.length> einen Ausgabetyp von `Int` , sodass die Ausgabe zuerst in eine konvertiert werden muss, `Double` bevor Sie als Teil eines Gleit Komma Ausdrucks verwendet werden kann.
Dies kann mithilfe der- <xref:microsoft.quantum.convert.intasdouble> Funktion erfolgen:

```qsharp
open Microsoft.Quantum.Convert as Convert;

function HalfLength<'T>(arr : 'T[]) : Double {
    return Convert.IntAsDouble(Length(arr)) / 2.0;
}
```

Der- <xref:microsoft.quantum.convert> Namespace stellt allgemeine Typkonvertierungs Funktionen zum Arbeiten mit den grundlegenden integrierten Typen wie `Int` , `Double` , `BigInt` , und bereit `Result` `Bool` :

```qsharp
let bool = Convert.ResultAsBool(One);        // true
let big = Convert.IntAsBigInt(271);          // 271L
let indices = Convert.RangeAsIntArray(0..4); // [0, 1, 2, 3, 4]
```

Der- <xref:microsoft.quantum.convert> Namespace bietet auch einige exotischere Konvertierungen, wie z `FunctionAsOperation` . b., die Funktionen `'T -> 'U` in neue Vorgänge konvertieren `'T => 'U` .

Schließlich bietet die Q# Standardbibliothek eine Reihe von benutzerdefinierten Typen, z. b <xref:microsoft.quantum.math.complex> <xref:microsoft.quantum.arithmetic.littleendian> . und.
Zusammen mit diesen Typen bietet die Standardbibliothek Funktionen wie z. b. <xref:microsoft.quantum.arithmetic.bigendianaslittleendian> :

```Q#
open Microsoft.Quantum.Arithmetic as Arithmetic;

let register = Arithmetic.BigEndian(qubits);
IncrementByInteger(Arithmetic.BigEndianAsLittleEndian(register));
```
