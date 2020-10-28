---
uid: Microsoft.Quantum.Math.ArgComplex
title: Argcomplex-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ArgComplex
qsharp.summary: Returns the phase of a complex number of type `Complex`.
ms.openlocfilehash: 629aa32ad80e5aa3d6f5ff75ac65df9b1a96fc15
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92723269"
---
# <a name="argcomplex-function"></a>Argcomplex-Funktion

Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)

Paketen [](https://nuget.org/packages/)


Gibt die Phase einer komplexen Zahl vom Typ zurück `Complex` .

```qsharp
function ArgComplex (input : Microsoft.Quantum.Math.Complex) : Double
```


## <a name="input"></a>Eingabe

### <a name="input--complex"></a>Eingabe: [Komplex](xref:Microsoft.Quantum.Math.Complex)

Komplexe Zahl $c = x + i y $.



## <a name="output--double"></a>Ausgabe: [Double](xref:microsoft.quantum.lang-ref.double)

Phase $ \text{Arg} [c] = \text{ARCTAN} (y, x) \in (-\pi, \pi] $.