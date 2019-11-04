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
# <a name="type-conversions"></a><span data-ttu-id="3ddbe-103">Typkonvertierungen</span><span class="sxs-lookup"><span data-stu-id="3ddbe-103">Type Conversions</span></span> #

<span data-ttu-id="3ddbe-104">F # ist eine **stark typisierte** Sprache.</span><span class="sxs-lookup"><span data-stu-id="3ddbe-104">Q# is a **strongly-typed** language.</span></span>
<span data-ttu-id="3ddbe-105">Insbesondere wird Q # nicht implizit zwischen unterschiedlichen Typen umgewandelt.</span><span class="sxs-lookup"><span data-stu-id="3ddbe-105">In particular, Q# does not implicitly cast between distinct types.</span></span> <span data-ttu-id="3ddbe-106">Beispielsweise ist `1 + 2.0` kein gültiger Q #-Ausdruck.</span><span class="sxs-lookup"><span data-stu-id="3ddbe-106">For instance, `1 + 2.0` is not a valid Q# expression.</span></span>
<span data-ttu-id="3ddbe-107">Stattdessen bietet Q # eine Vielzahl von Typkonvertierungs Funktionen zum Erstellen neuer Werte eines bestimmten Typs.</span><span class="sxs-lookup"><span data-stu-id="3ddbe-107">Rather, Q# provides a variety of type conversion functions for constructing new values of a given type.</span></span>

<span data-ttu-id="3ddbe-108"><xref:microsoft.quantum.core.length> hat z. b. den Ausgabetyp `Int`, sodass die Ausgabe zuerst in eine `Double` konvertiert werden muss, bevor Sie als Teil eines Gleit Komma Ausdrucks verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="3ddbe-108">For example, <xref:microsoft.quantum.core.length> has an output type of `Int`, so its output must first be converted to a `Double` before it can be used as a part of a floating-point expression.</span></span>
<span data-ttu-id="3ddbe-109">Dies kann mithilfe der <xref:microsoft.quantum.convert.intasdouble>-Funktion erfolgen:</span><span class="sxs-lookup"><span data-stu-id="3ddbe-109">This can be done using the <xref:microsoft.quantum.convert.intasdouble> function:</span></span>

```qsharp
open Microsoft.Quantum.Convert as Convert;

function HalfLength<'T>(arr : 'T[]) : Double {
    return Convert.IntAsDouble(Length(arr)) / 2.0;
}
```

<span data-ttu-id="3ddbe-110">Der <xref:microsoft.quantum.convert>-Namespace stellt allgemeine Typkonvertierungs Funktionen zum Arbeiten mit den grundlegenden integrierten Typen bereit, z. b. `Int`, `Double`, `BigInt`, `Result`und `Bool`:</span><span class="sxs-lookup"><span data-stu-id="3ddbe-110">The <xref:microsoft.quantum.convert> namespace provides common type conversion functions for working with the basic built-in types, such as `Int`, `Double`, `BigInt`, `Result`, and `Bool`:</span></span>

```qsharp
let bool = Convert.ResultAsBool(One);        // true
let big = Convert.IntAsBigInt(271);          // 271L
let indices = Convert.RangeAsIntArray(0..4); // [0, 1, 2, 3, 4]
```

<span data-ttu-id="3ddbe-111">Der <xref:microsoft.quantum.convert>-Namespace bietet auch einige exotischere Konvertierungen, z. b. `FunctionAsOperation`, mit denen Funktionen `'T -> 'U` in neue Vorgänge `'T => 'U`konvertiert werden.</span><span class="sxs-lookup"><span data-stu-id="3ddbe-111">The <xref:microsoft.quantum.convert> namespace also provides some more exotic conversions, such as `FunctionAsOperation`, which converts functions `'T -> 'U` into new operations `'T => 'U`.</span></span>

<span data-ttu-id="3ddbe-112">Zum Schluss bietet die Q #-Standardbibliothek eine Reihe von benutzerdefinierten Typen, z. b. <xref:microsoft.quantum.math.complex> und <xref:microsoft.quantum.arithmetic.littleendian>.</span><span class="sxs-lookup"><span data-stu-id="3ddbe-112">Finally, the Q# standard library provides a number of user-defined types such as <xref:microsoft.quantum.math.complex> and <xref:microsoft.quantum.arithmetic.littleendian>.</span></span>
<span data-ttu-id="3ddbe-113">Zusammen mit diesen Typen bietet die Standardbibliothek Funktionen wie <xref:microsoft.quantum.arithmetic.bigendianaslittleendian>:</span><span class="sxs-lookup"><span data-stu-id="3ddbe-113">Along with these types, the standard library provides functions such as <xref:microsoft.quantum.arithmetic.bigendianaslittleendian>:</span></span>

```Q#
open Microsoft.Quantum.Arithmetic as Arithmetic;

let register = Arithmetic.BigEndian(qubits);
IncrementByInteger(Arithmetic.BigEndianAsLittleEndian(register));
```
