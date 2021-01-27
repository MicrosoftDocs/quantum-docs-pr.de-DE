---
uid: Microsoft.Quantum.Diagnostics.AllEqualityFactI
title: Allequalityfakti-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AllEqualityFactI
qsharp.summary: Asserts that two arrays of integer values are equal.
ms.openlocfilehash: a7043b9c670f79e270180c583fef56b70c1a3bcb
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98830890"
---
# <a name="allequalityfacti-function"></a>Allequalityfakti-Funktion

Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Bestätigt, dass zwei Arrays von ganzzahligen Werten gleich sind.

```qsharp
function AllEqualityFactI (actual : Int[], expected : Int[], message : String) : Unit
```


## <a name="input"></a>Eingabe

### <a name="actual--int"></a>tatsächlicher Wert: [int](xref:microsoft.quantum.lang-ref.int)[]

Das Array, das von einem interessanten Testfall erzeugt wird.


### <a name="expected--int"></a>erwartet: [int](xref:microsoft.quantum.lang-ref.int)[]

Das Array, das von einem interessanten Testfall erwartet wird.


### <a name="message--string"></a>Message: [Zeichenfolge](xref:microsoft.quantum.lang-ref.string)

Eine Meldung, die gedruckt werden soll, wenn die Arrays nicht gleich sind.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)

