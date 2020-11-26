---
uid: Microsoft.Quantum.Diagnostics.Contradiction
title: Widerspruch Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: Contradiction
qsharp.summary: Declares that a classical condition is false.
ms.openlocfilehash: f9ad9a7d67bda8e50c76f679f535ad55ba07698e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96202140"
---
# <a name="contradiction-function"></a>Widerspruch Funktion

Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


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