---
uid: Microsoft.Quantum.Logical.Not
title: Not-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: Not
qsharp.summary: Returns the Boolean negation of a value.
ms.openlocfilehash: f2db43f4a2ce83d8cad1d60aa8c481a33b0c7d44
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96197448"
---
# <a name="not-function"></a>Not-Funktion

Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Gibt die boolesche Negation eines Werts zurück.

```qsharp
function Not (value : Bool) : Bool
```


## <a name="input"></a>Eingabe

### <a name="value--bool"></a>Wert: [bool](xref:microsoft.quantum.lang-ref.bool)

Der Wert, der negiert werden soll.



## <a name="output--bool"></a>Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)

`true` nur dann, wenn den Wert hat `value` `false` .

## <a name="remarks"></a>Bemerkungen

Die folgenden sind gleichwertig:

```Q#
let x = not value;
let x = Not(value);
```