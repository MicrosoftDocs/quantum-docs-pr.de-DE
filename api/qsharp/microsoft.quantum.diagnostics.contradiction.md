---
uid: Microsoft.Quantum.Diagnostics.Contradiction
title: Widerspruch Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: Contradiction
qsharp.summary: Declares that a classical condition is false.
ms.openlocfilehash: 7d62c9341b768dfdfbfbf8e73e64748f04317595
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98829364"
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



## <a name="example"></a>Beispiel

Der folgende f #-Code druckt "Hello, World":

```qsharp
Contradiction(2 == 3, "2 is not equal to 3.");
Message("Hello, world.");
```

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Diagnostics. Fact](xref:Microsoft.Quantum.Diagnostics.Fact)