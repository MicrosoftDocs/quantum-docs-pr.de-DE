---
uid: Microsoft.Quantum.Core.RangeEnd
title: RangeEnd-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Core
qsharp.name: RangeEnd
qsharp.summary: Returns the defined end value of the given range, which is not necessarily the last element in the sequence.
ms.openlocfilehash: 4dbcf517c4dc17775040444c77deb0e449082390
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702870"
---
# <a name="rangeend-function"></a>RangeEnd-Funktion

Namespace: [Microsoft. Quantum. Core](xref:Microsoft.Quantum.Core)

Paketen [](https://nuget.org/packages/)


Gibt den definierten Endwert des angegebenen Bereichs zurück, der nicht notwendigerweise das letzte Element in der Sequenz ist.

```qsharp
function RangeEnd (range : Range) : Int
```


## <a name="input"></a>Eingabe

### <a name="range--range"></a>Bereich: [Bereich](xref:microsoft.quantum.lang-ref.range)





## <a name="output--int"></a>Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)

Der definierte Endwert des angegebenen Bereichs.

## <a name="remarks"></a>Hinweise

Das erste Element eines Bereichs Ausdrucks ist `start` , sein zweites Element `start+step` , das dritte Element ist `start+step+step` usw., bis erfolgreich `end` ist.

Beachten Sie, dass sich der definierte Endwert eines Bereichs von dem letzten Element in der Sequenz unterscheiden kann, die durch den Bereich angegeben wird. beispielsweise in einem Bereich von 0. 2.. 5 das letzte Element ist 4, der Endwert ist jedoch 5.