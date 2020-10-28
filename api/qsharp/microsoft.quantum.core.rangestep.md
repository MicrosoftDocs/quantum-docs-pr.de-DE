---
uid: Microsoft.Quantum.Core.RangeStep
title: Rangestep-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Core
qsharp.name: RangeStep
qsharp.summary: Returns the integer that specifies how the next value of a range is calculated.
ms.openlocfilehash: f8e4c42330f2d6afdc1c0a9bdde36081ccab2f94
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702834"
---
# <a name="rangestep-function"></a>Rangestep-Funktion

Namespace: [Microsoft. Quantum. Core](xref:Microsoft.Quantum.Core)

Paketen [](https://nuget.org/packages/)


Gibt die ganze Zahl zurück, die angibt, wie der nächste Wert eines Bereichs berechnet wird.

```qsharp
function RangeStep (range : Range) : Int
```


## <a name="input"></a>Eingabe

### <a name="range--range"></a>Bereich: [Bereich](xref:microsoft.quantum.lang-ref.range)





## <a name="output--int"></a>Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)

Der definierte Schrittwert des angegebenen Bereichs.

## <a name="remarks"></a>Hinweise

Das erste Element eines Bereichs Ausdrucks ist `start` , sein zweites Element `start+step` , das dritte Element ist `start+step+step` usw., bis erfolgreich `end` ist.