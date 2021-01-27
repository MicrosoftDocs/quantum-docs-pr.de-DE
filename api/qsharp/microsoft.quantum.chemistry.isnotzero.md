---
uid: Microsoft.Quantum.Chemistry.IsNotZero
title: Isnotzero-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry
qsharp.name: IsNotZero
qsharp.summary: Checks whether a `Double` number is not approximately zero.
ms.openlocfilehash: 9384e5dafd4b5b7d44cb348c9537ebc2c621466d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98839598"
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