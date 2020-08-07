---
title: Typkonvertierungen in den Q# Standardbibliotheken
description: Erfahren Sie mehr über gängige und benutzerdefinierte Typkonvertierungs Funktionen in den Q# Standardbibliotheken.
author: cgranade
uid: microsoft.quantum.libraries.convert
ms.author: chgranad@microsoft.com
ms.topic: article
no-loc:
- Q#
- $$v
ms.openlocfilehash: 2319bf453f5fbf6bd068859ea65562423d3ff4d0
ms.sourcegitcommit: 6bf99d93590d6aa80490e88f2fd74dbbee8e0371
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2020
ms.locfileid: "87868510"
---
# <a name="type-conversions"></a><span data-ttu-id="44eec-103">Typkonvertierungen</span><span class="sxs-lookup"><span data-stu-id="44eec-103">Type Conversions</span></span> #

<span data-ttu-id="44eec-104">Q#ist eine **stark typisierte** Sprache.</span><span class="sxs-lookup"><span data-stu-id="44eec-104">Q# is a **strongly-typed** language.</span></span>
<span data-ttu-id="44eec-105">Insbesondere wird Q# nicht implizit zwischen unterschiedlichen Typen umgewandelt.</span><span class="sxs-lookup"><span data-stu-id="44eec-105">In particular, Q# does not implicitly cast between distinct types.</span></span> <span data-ttu-id="44eec-106">Beispielsweise `1 + 2.0` ist kein gültiger Q# Ausdruck.</span><span class="sxs-lookup"><span data-stu-id="44eec-106">For instance, `1 + 2.0` is not a valid Q# expression.</span></span>
<span data-ttu-id="44eec-107">Stattdessen Q# stellt eine Reihe von Typkonvertierungs Funktionen zum Erstellen neuer Werte eines angegebenen Typs bereit.</span><span class="sxs-lookup"><span data-stu-id="44eec-107">Rather, Q# provides a variety of type conversion functions for constructing new values of a given type.</span></span>

<span data-ttu-id="44eec-108">Hat z. b. <xref:microsoft.quantum.core.length> einen Ausgabetyp von `Int` , sodass die Ausgabe zuerst in eine konvertiert werden muss, `Double` bevor Sie als Teil eines Gleit Komma Ausdrucks verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="44eec-108">For example, <xref:microsoft.quantum.core.length> has an output type of `Int`, so its output must first be converted to a `Double` before it can be used as a part of a floating-point expression.</span></span>
<span data-ttu-id="44eec-109">Dies kann mithilfe der- <xref:microsoft.quantum.convert.intasdouble> Funktion erfolgen:</span><span class="sxs-lookup"><span data-stu-id="44eec-109">This can be done using the <xref:microsoft.quantum.convert.intasdouble> function:</span></span>

```qsharp
open Microsoft.Quantum.Convert as Convert;

function HalfLength<'T>(arr : 'T[]) : Double {
    return Convert.IntAsDouble(Length(arr)) / 2.0;
}
```

<span data-ttu-id="44eec-110">Der- <xref:microsoft.quantum.convert> Namespace stellt allgemeine Typkonvertierungs Funktionen zum Arbeiten mit den grundlegenden integrierten Typen wie `Int` , `Double` , `BigInt` , und bereit `Result` `Bool` :</span><span class="sxs-lookup"><span data-stu-id="44eec-110">The <xref:microsoft.quantum.convert> namespace provides common type conversion functions for working with the basic built-in types, such as `Int`, `Double`, `BigInt`, `Result`, and `Bool`:</span></span>

```qsharp
let bool = Convert.ResultAsBool(One);        // true
let big = Convert.IntAsBigInt(271);          // 271L
let indices = Convert.RangeAsIntArray(0..4); // [0, 1, 2, 3, 4]
```

<span data-ttu-id="44eec-111">Der- <xref:microsoft.quantum.convert> Namespace bietet auch einige exotischere Konvertierungen, wie z `FunctionAsOperation` . b., die Funktionen `'T -> 'U` in neue Vorgänge konvertieren `'T => 'U` .</span><span class="sxs-lookup"><span data-stu-id="44eec-111">The <xref:microsoft.quantum.convert> namespace also provides some more exotic conversions, such as `FunctionAsOperation`, which converts functions `'T -> 'U` into new operations `'T => 'U`.</span></span>

<span data-ttu-id="44eec-112">Schließlich bietet die Q# Standardbibliothek eine Reihe von benutzerdefinierten Typen, z. b <xref:microsoft.quantum.math.complex> <xref:microsoft.quantum.arithmetic.littleendian> . und.</span><span class="sxs-lookup"><span data-stu-id="44eec-112">Finally, the Q# standard library provides a number of user-defined types such as <xref:microsoft.quantum.math.complex> and <xref:microsoft.quantum.arithmetic.littleendian>.</span></span>
<span data-ttu-id="44eec-113">Zusammen mit diesen Typen bietet die Standardbibliothek Funktionen wie z. b. <xref:microsoft.quantum.arithmetic.bigendianaslittleendian> :</span><span class="sxs-lookup"><span data-stu-id="44eec-113">Along with these types, the standard library provides functions such as <xref:microsoft.quantum.arithmetic.bigendianaslittleendian>:</span></span>

```Q#
open Microsoft.Quantum.Arithmetic as Arithmetic;

let register = Arithmetic.BigEndian(qubits);
IncrementByInteger(Arithmetic.BigEndianAsLittleEndian(register));
```
