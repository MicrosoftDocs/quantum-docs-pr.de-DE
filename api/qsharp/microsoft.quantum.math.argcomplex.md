---
uid: Microsoft.Quantum.Math.ArgComplex
title: Argcomplex-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ArgComplex
qsharp.summary: Returns the phase of a complex number of type `Complex`.
ms.openlocfilehash: 259296f397207cde4a7d6dfe6cfb1a18e8055216
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96211099"
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