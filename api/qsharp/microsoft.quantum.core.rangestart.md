---
uid: Microsoft.Quantum.Core.RangeStart
title: RangeStart-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Core
qsharp.name: RangeStart
qsharp.summary: Returns the defined start value of the given range.
ms.openlocfilehash: 5b04e8c860a4bd6af7b10b4dbf803b1eb69ef5d8
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98831112"
---
# <a name="rangestart-function"></a>RangeStart-Funktion

Namespace: [Microsoft. Quantum. Core](xref:Microsoft.Quantum.Core)

Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Gibt den definierten Startwert des angegebenen Bereichs zurück.

```qsharp
function RangeStart (range : Range) : Int
```


## <a name="input"></a>Eingabe

### <a name="range--range"></a>Bereich: [Bereich](xref:microsoft.quantum.lang-ref.range)





## <a name="output--int"></a>Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)

Der definierte Startwert des angegebenen Bereichs.

## <a name="remarks"></a>Bemerkungen

Das erste Element eines Bereichs Ausdrucks ist `start` , sein zweites Element `start+step` , das dritte Element ist `start+step+step` usw., bis erfolgreich `end` ist.

Beachten Sie, dass der definierte Startwert eines Bereichs mit dem ersten Element der Sequenz übereinstimmt, es sei denn, der Bereich gibt eine leere Sequenz an (z. b. 2.). 1).