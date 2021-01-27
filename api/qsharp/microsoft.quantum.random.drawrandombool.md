---
uid: Microsoft.Quantum.Random.DrawRandomBool
title: Drawrandombool-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: DrawRandomBool
qsharp.summary: Given a success probability, returns a single Bernoulli trial that is true with the given probability.
ms.openlocfilehash: 7c13f8305756421b8d07baf22ff87764efac0418
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853688"
---
# <a name="drawrandombool-operation"></a>Drawrandombool-Vorgang

Namespace: [Microsoft. Quantum. Random](xref:Microsoft.Quantum.Random)

Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Bei einer Erfolgswahrscheinlichkeit wird eine einzelne Bernoulli-Testversion zurückgegeben, die mit der angegebenen Wahrscheinlichkeit true ist.

```qsharp
operation DrawRandomBool (successProbability : Double) : Bool
```


## <a name="input"></a>Eingabe

### <a name="successprobability--double"></a>erfolgreiche Programmierung: [Double](xref:microsoft.quantum.lang-ref.double)

Die Wahrscheinlichkeit, mit der `true` zurückgegeben werden soll.



## <a name="output--bool"></a>Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)

`true` mit Wahrscheinlichkeit `successProbability` und `false` mit Wahrscheinlichkeit `1.0 - successProbability` .

## <a name="example"></a>Beispiel

Die folgenden Q # Ausschnitt-Beispiele werden aus einer unausgewogenen Münze gedreht:

```qsharp
let flips = DrawMany(DrawRandomBool, 10, 0.6);
```