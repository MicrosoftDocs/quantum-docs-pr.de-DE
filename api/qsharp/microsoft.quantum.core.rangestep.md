---
uid: Microsoft.Quantum.Core.RangeStep
title: Rangestep-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Core
qsharp.name: RangeStep
qsharp.summary: Returns the integer that specifies how the next value of a range is calculated.
ms.openlocfilehash: 39c8581fe795a1b76d2a6e81c238a271287c2c38
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96213802"
---
# <a name="rangestep-function"></a>Rangestep-Funktion

Namespace: [Microsoft. Quantum. Core](xref:Microsoft.Quantum.Core)

Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Gibt die ganze Zahl zurück, die angibt, wie der nächste Wert eines Bereichs berechnet wird.

```qsharp
function RangeStep (range : Range) : Int
```


## <a name="input"></a>Eingabe

### <a name="range--range"></a>Bereich: [Bereich](xref:microsoft.quantum.lang-ref.range)





## <a name="output--int"></a>Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)

Der definierte Schrittwert des angegebenen Bereichs.

## <a name="remarks"></a>Bemerkungen

Das erste Element eines Bereichs Ausdrucks ist `start` , sein zweites Element `start+step` , das dritte Element ist `start+step+step` usw., bis erfolgreich `end` ist.