---
uid: Microsoft.Quantum.Math.ArgComplex
title: Argcomplex-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ArgComplex
qsharp.summary: Returns the phase of a complex number of type `Complex`.
ms.openlocfilehash: e8ce73a43940ab0ed66338f962cc6f76fc2b694b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842754"
---
# <a name="argcomplex-function"></a>Argcomplex-Funktion

Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Gibt die Phase einer komplexen Zahl vom Typ zurück `Complex` .

```qsharp
function ArgComplex (input : Microsoft.Quantum.Math.Complex) : Double
```


## <a name="input"></a>Eingabe

### <a name="input--complex"></a>Eingabe: [Komplex](xref:Microsoft.Quantum.Math.Complex)

Komplexe Zahl $c = x + i y $.



## <a name="output--double"></a>Ausgabe: [Double](xref:microsoft.quantum.lang-ref.double)

Phase $ \text{Arg} [c] = \text{ARCTAN} (y, x) \in (-\pi, \pi] $.