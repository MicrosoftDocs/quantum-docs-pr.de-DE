---
title: 'Typkonvertierungen in den Q# Standardbibliotheken'
description: 'Erfahren Sie mehr über gängige und benutzerdefinierte Typkonvertierungs Funktionen in den Q# Standardbibliotheken.'
author: cgranade
uid: microsoft.quantum.libraries.convert
ms.author: chgranad
ms.topic: article
no-loc:
- 'Q#'
- '$$v'
ms.openlocfilehash: 9ec3a2ecd2aa59a10a7033e7b3067eb147ce4035
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92691102"
---
# <a name="type-conversions"></a><span data-ttu-id="515c7-103">Typkonvertierungen</span><span class="sxs-lookup"><span data-stu-id="515c7-103">Type Conversions</span></span> #

<span data-ttu-id="515c7-104">Q# ist eine **stark typisierte** Sprache.</span><span class="sxs-lookup"><span data-stu-id="515c7-104">Q# is a **strongly-typed** language.</span></span>
<span data-ttu-id="515c7-105">Insbesondere wird Q# nicht implizit zwischen unterschiedlichen Typen umgewandelt.</span><span class="sxs-lookup"><span data-stu-id="515c7-105">In particular, Q# does not implicitly cast between distinct types.</span></span> <span data-ttu-id="515c7-106">Beispielsweise `1 + 2.0` ist kein gültiger Q# Ausdruck.</span><span class="sxs-lookup"><span data-stu-id="515c7-106">For instance, `1 + 2.0` is not a valid Q# expression.</span></span>
<span data-ttu-id="515c7-107">Stattdessen Q# stellt eine Reihe von Typkonvertierungs Funktionen zum Erstellen neuer Werte eines angegebenen Typs bereit.</span><span class="sxs-lookup"><span data-stu-id="515c7-107">Rather, Q# provides a variety of type conversion functions for constructing new values of a given type.</span></span>

<span data-ttu-id="515c7-108">Hat z. b. <xref:Microsoft.Quantum.Core.Length> einen Ausgabetyp von `Int` , sodass die Ausgabe zuerst in eine konvertiert werden muss, `Double` bevor Sie als Teil eines Gleit Komma Ausdrucks verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="515c7-108">For example, <xref:Microsoft.Quantum.Core.Length> has an output type of `Int`, so its output must first be converted to a `Double` before it can be used as a part of a floating-point expression.</span></span>
<span data-ttu-id="515c7-109">Dies kann mithilfe der- <xref:Microsoft.Quantum.Convert.IntAsDouble> Funktion erfolgen:</span><span class="sxs-lookup"><span data-stu-id="515c7-109">This can be done using the <xref:Microsoft.Quantum.Convert.IntAsDouble> function:</span></span>

```qsharp
open Microsoft.Quantum.Convert as Convert;

function HalfLength<'T>(arr : 'T[]) : Double {
    return Convert.IntAsDouble(Length(arr)) / 2.0;
}
```

<span data-ttu-id="515c7-110">Der- <xref:Microsoft.Quantum.Convert> Namespace stellt allgemeine Typkonvertierungs Funktionen zum Arbeiten mit den grundlegenden integrierten Typen wie `Int` , `Double` , `BigInt` , und bereit `Result` `Bool` :</span><span class="sxs-lookup"><span data-stu-id="515c7-110">The <xref:Microsoft.Quantum.Convert> namespace provides common type conversion functions for working with the basic built-in types, such as `Int`, `Double`, `BigInt`, `Result`, and `Bool`:</span></span>

```qsharp
let bool = Convert.ResultAsBool(One);        // true
let big = Convert.IntAsBigInt(271);          // 271L
let indices = Convert.RangeAsIntArray(0..4); // [0, 1, 2, 3, 4]
```

<span data-ttu-id="515c7-111">Der- <xref:Microsoft.Quantum.Convert> Namespace bietet auch einige exotischere Konvertierungen, wie z `FunctionAsOperation` . b., die Funktionen `'T -> 'U` in neue Vorgänge konvertieren `'T => 'U` .</span><span class="sxs-lookup"><span data-stu-id="515c7-111">The <xref:Microsoft.Quantum.Convert> namespace also provides some more exotic conversions, such as `FunctionAsOperation`, which converts functions `'T -> 'U` into new operations `'T => 'U`.</span></span>

<span data-ttu-id="515c7-112">Schließlich bietet die Q# Standardbibliothek eine Reihe von benutzerdefinierten Typen, z. b <xref:Microsoft.Quantum.Math.Complex> <xref:Microsoft.Quantum.Arithmetic.LittleEndian> . und.</span><span class="sxs-lookup"><span data-stu-id="515c7-112">Finally, the Q# standard library provides a number of user-defined types such as <xref:Microsoft.Quantum.Math.Complex> and <xref:Microsoft.Quantum.Arithmetic.LittleEndian>.</span></span>
<span data-ttu-id="515c7-113">Zusammen mit diesen Typen bietet die Standardbibliothek Funktionen wie z. b. <xref:Microsoft.Quantum.Arithmetic.BigEndianAsLittleEndian> :</span><span class="sxs-lookup"><span data-stu-id="515c7-113">Along with these types, the standard library provides functions such as <xref:Microsoft.Quantum.Arithmetic.BigEndianAsLittleEndian>:</span></span>

```Q#
open Microsoft.Quantum.Arithmetic as Arithmetic;

let register = Arithmetic.BigEndian(qubits);
IncrementByInteger(Arithmetic.BigEndianAsLittleEndian(register));
```
