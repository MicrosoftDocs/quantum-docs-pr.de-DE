---
uid: Microsoft.Quantum.Diagnostics.Contradiction
title: Widerspruch Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: Contradiction
qsharp.summary: Declares that a classical condition is false.
ms.openlocfilehash: a5f3f26c5ada2eea9206699a2cc77575a9b5eebd
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702708"
---
# <a name="contradiction-function"></a>Widerspruch Funktion

Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Paketen [](https://nuget.org/packages/)


Deklariert, dass eine klassische Bedingung false ist.

```qsharp
function Contradiction (actual : Bool, message : String) : Unit
```


## <a name="input"></a>Eingabe

### <a name="actual--bool"></a>tatsächlicher Wert: [bool](xref:microsoft.quantum.lang-ref.bool)

Die zu deklarier Ende Bedingung.


### <a name="message--string"></a>Message: [Zeichenfolge](xref:microsoft.quantum.lang-ref.string)

Die Fehlermeldungs Zeichenfolge, die gedruckt werden soll, wenn die klassische Bedingung "true" ist.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Diagnostics. Fact](xref:Microsoft.Quantum.Diagnostics.Fact)