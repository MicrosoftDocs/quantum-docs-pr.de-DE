---
uid: Microsoft.Quantum.Diagnostics.EqualityWithinToleranceFact
title: Equalitywithintolerancefact-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: EqualityWithinToleranceFact
qsharp.summary: Represents the claim that a classical floating point value has the expected value up to a given absolute tolerance.
ms.openlocfilehash: de15a32d5b38c5ab8c681d2c052669a48cf676cc
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702659"
---
# <a name="equalitywithintolerancefact-function"></a>Equalitywithintolerancefact-Funktion

Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Paketen [](https://nuget.org/packages/)


Stellt den Anspruch dar, dass ein klassischer Gleit Komma Wert den erwarteten Wert bis zu einer bestimmten absoluten Toleranz aufweist.

```qsharp
function EqualityWithinToleranceFact (actual : Double, expected : Double, tolerance : Double) : Unit
```


## <a name="input"></a>Eingabe

### <a name="actual--double"></a>tatsächlicher Wert: [Double](xref:microsoft.quantum.lang-ref.double)

Die Zahl, die geprüft werden soll.


### <a name="expected--double"></a>erwartet: [Double](xref:microsoft.quantum.lang-ref.double)

Der erwartete Wert.


### <a name="tolerance--double"></a>Toleranz: [Double](xref:microsoft.quantum.lang-ref.double)

Absolute Toleranz für den Unterschied zwischen tatsächlichem und erwartetem Verhalten.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)

