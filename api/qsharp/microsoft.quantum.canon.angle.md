---
uid: Microsoft.Quantum.Canon.Angle
title: Angle-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Angle
qsharp.summary: Returns 1, if `index` has an odd number of 1s and -1, if `index` has an even number of 1s.
ms.openlocfilehash: 1d8a9c2c19469e4949f043edd1ba91021fa42e78
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96219412"
---
# <a name="angle-function"></a>Angle-Funktion

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Gibt 1 zurück, wenn `index` eine ungerade Zahl von 1 s und-1 aufweist, wenn `index` eine gerade Anzahl von 1 s hat.

```qsharp
function Angle (index : Int) : Int
```


## <a name="description"></a>BESCHREIBUNG

Der Wert entspricht dem Vorzeichen des Koeffizienten des Rademacher-Walsh Spektrums der n-Variablen und der Funktion für eine bestimmte Zuweisung, die den Winkel der Drehung bestimmt.

## <a name="input"></a>Eingabe

### <a name="index--int"></a>Index: [int](xref:microsoft.quantum.lang-ref.int)

Eingabe Zuweisung als Ganzzahl (von 0 bis 2 ^ n-1)



## <a name="output--int"></a>Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)

