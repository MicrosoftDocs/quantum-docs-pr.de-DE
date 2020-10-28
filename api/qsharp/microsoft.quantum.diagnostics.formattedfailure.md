---
uid: Microsoft.Quantum.Diagnostics.FormattedFailure
title: Formattedfailure-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: FormattedFailure
qsharp.summary: Internal function used to fail with meaningful error messages.
ms.openlocfilehash: 0d7fb01ddf23cd6d79f722c8f6b691afa74a8885
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702629"
---
# <a name="formattedfailure-function"></a>Formattedfailure-Funktion

Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Paketen [](https://nuget.org/packages/)


Interne Funktion, die verwendet wird, um mit aussagekräftigen Fehlermeldungen fehlschlägt

```qsharp
function FormattedFailure<'T> (actual : 'T, expected : 'T, message : String) : Unit
```


## <a name="input"></a>Eingabe

### <a name="actual--t"></a>tatsächlicher Wert: 't




### <a name="expected--t"></a>erwartet: 't




### <a name="message--string"></a>Message: [Zeichenfolge](xref:microsoft.quantum.lang-ref.string)





## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Typparameter

### <a name="t"></a>GIF



## <a name="remarks"></a>Hinweise

Diese Funktion soll von Simulationslauf Zeiten emuliert werden, um Weiterleitungs formatierte Widersprüche zuzulassen.