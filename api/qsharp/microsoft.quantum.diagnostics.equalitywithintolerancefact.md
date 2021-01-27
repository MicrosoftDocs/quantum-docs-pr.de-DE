---
uid: Microsoft.Quantum.Diagnostics.EqualityWithinToleranceFact
title: Equalitywithintolerancefact-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: EqualityWithinToleranceFact
qsharp.summary: Represents the claim that a classical floating point value has the expected value up to a given absolute tolerance.
ms.openlocfilehash: ab7e43d951bf741926b15f27f94d176e88609d4a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98828747"
---
# <a name="equalitywithintolerancefact-function"></a>Equalitywithintolerancefact-Funktion

Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


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

