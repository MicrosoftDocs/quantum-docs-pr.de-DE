---
title: Typkonvertierungen in den Q# Standardbibliotheken
description: Erfahren Sie mehr über gängige und benutzerdefinierte Typkonvertierungs Funktionen in den Q# Standardbibliotheken.
author: cgranade
uid: microsoft.quantum.libraries.convert
ms.author: chgranad
ms.topic: conceptual
no-loc:
- Q#
- $$v
ms.openlocfilehash: 67f47339363a52097f342c8ae4e43a8a93d606a8
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98858018"
---
# <a name="type-conversions"></a>Typkonvertierungen #

Q# ist eine **stark typisierte** Sprache.
Insbesondere wird Q# nicht implizit zwischen unterschiedlichen Typen umgewandelt. Beispielsweise `1 + 2.0` ist kein gültiger Q# Ausdruck.
Stattdessen Q# stellt eine Reihe von Typkonvertierungs Funktionen zum Erstellen neuer Werte eines angegebenen Typs bereit.

Hat z. b. <xref:Microsoft.Quantum.Core.Length> einen Ausgabetyp von `Int` , sodass die Ausgabe zuerst in eine konvertiert werden muss, `Double` bevor Sie als Teil eines Gleit Komma Ausdrucks verwendet werden kann.
Dies kann mithilfe der- <xref:Microsoft.Quantum.Convert.IntAsDouble> Funktion erfolgen:

```qsharp
open Microsoft.Quantum.Convert as Convert;

function HalfLength<'T>(arr : 'T[]) : Double {
    return Convert.IntAsDouble(Length(arr)) / 2.0;
}
```

Der- <xref:Microsoft.Quantum.Convert> Namespace stellt allgemeine Typkonvertierungs Funktionen zum Arbeiten mit den grundlegenden integrierten Typen wie `Int` , `Double` , `BigInt` , und bereit `Result` `Bool` :

```qsharp
let bool = Convert.ResultAsBool(One);        // true
let big = Convert.IntAsBigInt(271);          // 271L
let indices = Convert.RangeAsIntArray(0..4); // [0, 1, 2, 3, 4]
```

Der- <xref:Microsoft.Quantum.Convert> Namespace bietet auch einige exotischere Konvertierungen, wie z `FunctionAsOperation` . b., die Funktionen `'T -> 'U` in neue Vorgänge konvertieren `'T => 'U` .

Schließlich bietet die Q# Standardbibliothek eine Reihe von benutzerdefinierten Typen, z. b <xref:Microsoft.Quantum.Math.Complex> <xref:Microsoft.Quantum.Arithmetic.LittleEndian> . und.
Zusammen mit diesen Typen bietet die Standardbibliothek Funktionen wie z. b. <xref:Microsoft.Quantum.Arithmetic.BigEndianAsLittleEndian> :

```qsharp
open Microsoft.Quantum.Arithmetic as Arithmetic;

let register = Arithmetic.BigEndian(qubits);
IncrementByInteger(Arithmetic.BigEndianAsLittleEndian(register));
```
