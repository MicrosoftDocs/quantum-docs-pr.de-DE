---
uid: Microsoft.Quantum.Diagnostics.NearEqualityFactD
title: Netarequalityfaktd-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: NearEqualityFactD
qsharp.summary: Asserts that a classical floating point value has the expected value up to a small tolerance of 1e-10.
ms.openlocfilehash: 5acfe5043342fd88276910a9fd0347f7d2f6960f
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96201511"
---
# <a name="nearequalityfactd-function"></a>Netarequalityfaktd-Funktion

Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


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



## <a name="remarks"></a>Bemerkungen

Dies entspricht <xref:microsoft.quantum.diagnostics.equalitywithintolerancefact> der hart codierten Toleranz von $10 ^ {-10} $.