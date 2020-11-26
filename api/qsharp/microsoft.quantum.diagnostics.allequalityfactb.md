---
uid: Microsoft.Quantum.Diagnostics.AllEqualityFactB
title: Allequalityfaktb-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AllEqualityFactB
qsharp.summary: Asserts that two arrays of boolean values are equal.
ms.openlocfilehash: 79dcf65956ba9436fb6fdd452f22f35d4852d6f8
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96213700"
---
# <a name="allequalityfactb-function"></a>Allequalityfaktb-Funktion

Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Bestätigt, dass zwei Arrays von booleschen Werten gleich sind.

```qsharp
function AllEqualityFactB (actual : Bool[], expected : Bool[], message : String) : Unit
```


## <a name="input"></a>Eingabe

### <a name="actual--bool"></a>tatsächlicher Wert: [bool](xref:microsoft.quantum.lang-ref.bool)[]

Das Array, das von einem interessanten Testfall erzeugt wird.


### <a name="expected--bool"></a>erwartet: [bool](xref:microsoft.quantum.lang-ref.bool)[]

Das Array, das von einem interessanten Testfall erwartet wird.


### <a name="message--string"></a>Message: [Zeichenfolge](xref:microsoft.quantum.lang-ref.string)

Eine Meldung, die gedruckt werden soll, wenn die Arrays nicht gleich sind.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)

