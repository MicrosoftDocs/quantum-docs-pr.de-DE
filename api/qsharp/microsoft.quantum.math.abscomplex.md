---
uid: Microsoft.Quantum.Math.AbsComplex
title: Abscomplex-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: AbsComplex
qsharp.summary: Returns the absolute value of a complex number of type `Complex`.
ms.openlocfilehash: d9afb4b9b37b6cdd83bfd3829d3174d769c5f41b
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96211388"
---
# <a name="abscomplex-function"></a>Abscomplex-Funktion

Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Gibt den absoluten Wert einer komplexen Zahl vom Typ zurück `Complex` .

```qsharp
function AbsComplex (input : Microsoft.Quantum.Math.Complex) : Double
```


## <a name="input"></a>Eingabe

### <a name="input--complex"></a>Eingabe: [Komplex](xref:Microsoft.Quantum.Math.Complex)

Komplexe Zahl $c = x + i y $.



## <a name="output--double"></a>Ausgabe: [Double](xref:microsoft.quantum.lang-ref.double)

Absoluter Wert $ | c | = \sqrt{x ^ 2 + y ^ 2} $.