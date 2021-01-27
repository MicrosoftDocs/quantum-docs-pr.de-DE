---
uid: Microsoft.Quantum.Core.RangeReverse
title: Rangereverse-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Core
qsharp.name: RangeReverse
qsharp.summary: Returns a new range which is the reverse of the input range.
ms.openlocfilehash: f3b94d3c6fa6350a2c337f8bc8d889d24d87a85b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853656"
---
# <a name="rangereverse-function"></a>Rangereverse-Funktion

Namespace: [Microsoft. Quantum. Core](xref:Microsoft.Quantum.Core)

Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Gibt einen neuen Bereich zurück, bei dem es sich um den umgekehrten Bereich des Eingabe Bereichs handelt.

```qsharp
function RangeReverse (r : Range) : Range
```


## <a name="input"></a>Eingabe

### <a name="r--range"></a>r: [Bereich](xref:microsoft.quantum.lang-ref.range)

Eingabebereich.



## <a name="output--range"></a>Ausgabe: [Bereich](xref:microsoft.quantum.lang-ref.range)

Ein neuer Bereich, der das Gegenteil des angegebenen Bereichs ist.

## <a name="remarks"></a>Bemerkungen

Beachten Sie, dass der umgekehrte Bereich eines Bereichs nicht einfach " `end` .. `-step` .." ist `start` , da das tatsächliche letzte Element eines Bereichs möglicherweise nicht mit identisch `end` ist.