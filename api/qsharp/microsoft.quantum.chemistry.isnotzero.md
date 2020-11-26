---
uid: Microsoft.Quantum.Chemistry.IsNotZero
title: Isnotzero-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry
qsharp.name: IsNotZero
qsharp.summary: Checks whether a `Double` number is not approximately zero.
ms.openlocfilehash: f80dbba6a51e62970e87c2782faba558340d2bd8
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96204061"
---
# <a name="isnotzero-function"></a>Isnotzero-Funktion

Namespace: [Microsoft. Quantum. Chemistry](xref:Microsoft.Quantum.Chemistry)

Paket: [Microsoft. Quantum. Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)


Überprüft, ob eine `Double` Zahl nicht ungefähr 0 (null) ist.

```qsharp
function IsNotZero (number : Double) : Bool
```


## <a name="input"></a>Eingabe

### <a name="number--double"></a>Zahl: [Double](xref:microsoft.quantum.lang-ref.double)

Zu überprüfende Zahl



## <a name="output--bool"></a>Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)

Gibt true zurück, wenn `number` einen absoluten Wert hat, der größer als ist `1e-15` .