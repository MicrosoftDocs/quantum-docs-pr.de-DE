---
uid: Microsoft.Quantum.Chemistry.IsNotZero
title: Isnotzero-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry
qsharp.name: IsNotZero
qsharp.summary: Checks whether a `Double` number is not approximately zero.
ms.openlocfilehash: 3c0f9c6695e8c9ec4a0953d5217c28c512ac7de1
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703548"
---
# <a name="isnotzero-function"></a>Isnotzero-Funktion

Namespace: [Microsoft. Quantum. Chemistry](xref:Microsoft.Quantum.Chemistry)

Paketen [](https://nuget.org/packages/)


Überprüft, ob eine `Double` Zahl nicht ungefähr 0 (null) ist.

```qsharp
function IsNotZero (number : Double) : Bool
```


## <a name="input"></a>Eingabe

### <a name="number--double"></a>Zahl: [Double](xref:microsoft.quantum.lang-ref.double)

Zu überprüfende Zahl



## <a name="output--bool"></a>Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)

Gibt true zurück, wenn `number` einen absoluten Wert hat, der größer als ist `1e-15` .