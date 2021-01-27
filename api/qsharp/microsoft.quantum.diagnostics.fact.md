---
uid: Microsoft.Quantum.Diagnostics.Fact
title: Fact-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: Fact
qsharp.summary: Declares that a classical condition is true.
ms.openlocfilehash: 8e86000f04c01040d420c2f682fc1b4ccf35cf39
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853322"
---
# <a name="fact-function"></a>Fact-Funktion

Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Deklariert, dass eine klassische Bedingung true ist.

```qsharp
function Fact (actual : Bool, message : String) : Unit
```


## <a name="input"></a>Eingabe

### <a name="actual--bool"></a>tatsächlicher Wert: [bool](xref:microsoft.quantum.lang-ref.bool)

Die zu deklarier Ende Bedingung.


### <a name="message--string"></a>Message: [Zeichenfolge](xref:microsoft.quantum.lang-ref.string)

Die Fehlermeldungs Zeichenfolge, die gedruckt werden soll, wenn die klassische Bedingung false ist.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="example"></a>Beispiel

Der folgende f #-Code Ausschnitt schlägt fehl:

```qsharp
Fact(false, "Expected true.");
```

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Diagnostics. Widersprüchlichkeit](xref:Microsoft.Quantum.Diagnostics.Contradiction)