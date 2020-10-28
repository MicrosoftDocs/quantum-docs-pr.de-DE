---
uid: Microsoft.Quantum.Math.SquaredNorm
title: Squarednorm-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: SquaredNorm
qsharp.summary: Returns the squared 2-norm of a vector.
ms.openlocfilehash: 4165a761753f336cb7b94ad36b11ac324ad4e5c6
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92725020"
---
# <a name="squarednorm-function"></a>Squarednorm-Funktion

Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)

Paketen [](https://nuget.org/packages/)


Gibt den quadratischen 2-Norm eines Vektors zurück.

```qsharp
function SquaredNorm (array : Double[]) : Double
```


## <a name="description"></a>BESCHREIBUNG

Gibt den quadratischen 2-Norm eines Vektors zurück. Das heißt, dass bei Angabe der Eingabe $ \vec{x} $ $ \ sum_i x_i ^ 2 $ zurückgegeben wird.

## <a name="input"></a>Eingabe

### <a name="array--double"></a>Array: [Double](xref:microsoft.quantum.lang-ref.double)[]

Der Vektor, dessen Quadrats 2-Norm zurückgegeben werden soll.



## <a name="output--double"></a>Ausgabe: [Double](xref:microsoft.quantum.lang-ref.double)

Die Quadrat-2-Norm von `array` .