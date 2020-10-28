---
uid: Microsoft.Quantum.Logical.Not
title: Not-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: Not
qsharp.summary: Returns the Boolean negation of a value.
ms.openlocfilehash: 3a688aac0178a2f4127496c1009fe7d5ee7ae198
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92701423"
---
# <a name="not-function"></a>Not-Funktion

Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)

Paketen [](https://nuget.org/packages/)


Gibt die boolesche Negation eines Werts zurück.

```qsharp
function Not (value : Bool) : Bool
```


## <a name="input"></a>Eingabe

### <a name="value--bool"></a>Wert: [bool](xref:microsoft.quantum.lang-ref.bool)

Der Wert, der negiert werden soll.



## <a name="output--bool"></a>Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)

`true` nur dann, wenn den Wert hat `value` `false` .

## <a name="remarks"></a>Hinweise

Die folgenden sind gleichwertig:

```Q#
let x = not value;
let x = Not(value);
```