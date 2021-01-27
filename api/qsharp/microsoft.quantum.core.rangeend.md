---
uid: Microsoft.Quantum.Core.RangeEnd
title: RangeEnd-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Core
qsharp.name: RangeEnd
qsharp.summary: Returns the defined end value of the given range, which is not necessarily the last element in the sequence.
ms.openlocfilehash: 196fab0bd97a441a16976033dc0d660c54cdfd6a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98831363"
---
# <a name="rangeend-function"></a>RangeEnd-Funktion

Namespace: [Microsoft. Quantum. Core](xref:Microsoft.Quantum.Core)

Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Gibt den definierten Endwert des angegebenen Bereichs zurück, der nicht notwendigerweise das letzte Element in der Sequenz ist.

```qsharp
function RangeEnd (range : Range) : Int
```


## <a name="input"></a>Eingabe

### <a name="range--range"></a>Bereich: [Bereich](xref:microsoft.quantum.lang-ref.range)





## <a name="output--int"></a>Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)

Der definierte Endwert des angegebenen Bereichs.

## <a name="remarks"></a>Bemerkungen

Das erste Element eines Bereichs Ausdrucks ist `start` , sein zweites Element `start+step` , das dritte Element ist `start+step+step` usw., bis erfolgreich `end` ist.

Beachten Sie, dass sich der definierte Endwert eines Bereichs von dem letzten Element in der Sequenz unterscheiden kann, die durch den Bereich angegeben wird. beispielsweise in einem Bereich von 0. 2.. 5 das letzte Element ist 4, der Endwert ist jedoch 5.