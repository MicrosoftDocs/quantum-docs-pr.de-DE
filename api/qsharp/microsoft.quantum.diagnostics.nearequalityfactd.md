---
uid: Microsoft.Quantum.Diagnostics.NearEqualityFactD
title: Netarequalityfaktd-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: NearEqualityFactD
qsharp.summary: Asserts that a classical floating point value has the expected value up to a small tolerance of 1e-10.
ms.openlocfilehash: d632a7a12c9ebbebfbc7939f2b8a24de8ae1ba2a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98827906"
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