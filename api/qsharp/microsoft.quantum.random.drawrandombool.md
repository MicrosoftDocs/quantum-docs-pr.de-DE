---
uid: Microsoft.Quantum.Random.DrawRandomBool
title: Drawrandombool-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: DrawRandomBool
qsharp.summary: Given a success probability, returns a single Bernoulli trial that is true with the given probability.
ms.openlocfilehash: 05cf8ad939691aac90625c5d056ea79aa062f553
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706714"
---
# <a name="drawrandombool-operation"></a>Drawrandombool-Vorgang

Namespace: [Microsoft. Quantum. Random](xref:Microsoft.Quantum.Random)

Paketen [](https://nuget.org/packages/)


Bei einer Erfolgswahrscheinlichkeit wird eine einzelne Bernoulli-Testversion zurückgegeben, die mit der angegebenen Wahrscheinlichkeit true ist.

```qsharp
operation DrawRandomBool (successProbability : Double) : Bool
```


## <a name="input"></a>Eingabe

### <a name="successprobability--double"></a>erfolgreiche Programmierung: [Double](xref:microsoft.quantum.lang-ref.double)

Die Wahrscheinlichkeit, mit der `true` zurückgegeben werden soll.



## <a name="output--bool"></a>Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)

`true` mit Wahrscheinlichkeit `successProbability` und `false` mit Wahrscheinlichkeit `1.0 - successProbability` .