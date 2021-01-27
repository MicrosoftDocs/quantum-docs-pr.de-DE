---
uid: Microsoft.Quantum.Math.SquaredNorm
title: Squarednorm-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: SquaredNorm
qsharp.summary: Returns the squared 2-norm of a vector.
ms.openlocfilehash: 72ae8266492bef64eaec34cd70c5fe725ee1e8c9
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848216"
---
# <a name="squarednorm-function"></a>Squarednorm-Funktion

Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Gibt den quadratischen 2-Norm eines Vektors zurück.

```qsharp
function SquaredNorm (array : Double[]) : Double
```


## <a name="description"></a>Beschreibung

Gibt den quadratischen 2-Norm eines Vektors zurück. Das heißt, dass bei Angabe der Eingabe $ \vec{x} $ $ \ sum_i x_i ^ 2 $ zurückgegeben wird.

## <a name="input"></a>Eingabe

### <a name="array--double"></a>Array: [Double](xref:microsoft.quantum.lang-ref.double)[]

Der Vektor, dessen Quadrats 2-Norm zurückgegeben werden soll.



## <a name="output--double"></a>Ausgabe: [Double](xref:microsoft.quantum.lang-ref.double)

Die Quadrat-2-Norm von `array` .