---
uid: Microsoft.Quantum.Diagnostics.NearEqualityFactD
title: Netarequalityfaktd-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: NearEqualityFactD
qsharp.summary: Asserts that a classical floating point value has the expected value up to a small tolerance of 1e-10.
ms.openlocfilehash: 5b55f515b27667071218a3f604ef703a6a15206d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702617"
---
# <a name="nearequalityfactd-function"></a>Netarequalityfaktd-Funktion

Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Paketen [](https://nuget.org/packages/)


Bestätigt, dass ein klassischer Gleit Komma Wert den erwarteten Wert bis zu einer kleinen Toleranz von 1E-10 aufweist.

```qsharp
function NearEqualityFactD (actual : Double, expected : Double) : Unit
```


## <a name="input"></a>Eingabe

### <a name="actual--double"></a>tatsächlicher Wert: [Double](xref:microsoft.quantum.lang-ref.double)

Die Zahl, die geprüft werden soll.


### <a name="expected--double"></a>erwartet: [Double](xref:microsoft.quantum.lang-ref.double)

Der erwartete Wert.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Hinweise

Dies entspricht <xref:microsoft.quantum.diagnostics.equalitywithintolerancefact> der hart codierten Toleranz von $10 ^ {-10} $.