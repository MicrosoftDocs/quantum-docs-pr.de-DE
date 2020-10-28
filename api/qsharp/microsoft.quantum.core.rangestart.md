---
uid: Microsoft.Quantum.Core.RangeStart
title: RangeStart-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Core
qsharp.name: RangeStart
qsharp.summary: Returns the defined start value of the given range.
ms.openlocfilehash: 3e4b0cebe34b4c98cb1d582a9cd11b46ff778517
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702839"
---
# <a name="rangestart-function"></a>RangeStart-Funktion

Namespace: [Microsoft. Quantum. Core](xref:Microsoft.Quantum.Core)

Paketen [](https://nuget.org/packages/)


Gibt den definierten Startwert des angegebenen Bereichs zurück.

```qsharp
function RangeStart (range : Range) : Int
```


## <a name="input"></a>Eingabe

### <a name="range--range"></a>Bereich: [Bereich](xref:microsoft.quantum.lang-ref.range)





## <a name="output--int"></a>Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)

Der definierte Startwert des angegebenen Bereichs.

## <a name="remarks"></a>Hinweise

Das erste Element eines Bereichs Ausdrucks ist `start` , sein zweites Element `start+step` , das dritte Element ist `start+step+step` usw., bis erfolgreich `end` ist.

Beachten Sie, dass der definierte Startwert eines Bereichs mit dem ersten Element der Sequenz übereinstimmt, es sei denn, der Bereich gibt eine leere Sequenz an (z. b. 2.). 1).