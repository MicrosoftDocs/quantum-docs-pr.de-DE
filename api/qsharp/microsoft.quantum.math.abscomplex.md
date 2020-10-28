---
uid: Microsoft.Quantum.Math.AbsComplex
title: Abscomplex-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: AbsComplex
qsharp.summary: Returns the absolute value of a complex number of type `Complex`.
ms.openlocfilehash: d47e04616d4bcf49273bec31fc22990a8244962b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92723886"
---
# <a name="abscomplex-function"></a>Abscomplex-Funktion

Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)

Paketen [](https://nuget.org/packages/)


Gibt den absoluten Wert einer komplexen Zahl vom Typ zurück `Complex` .

```qsharp
function AbsComplex (input : Microsoft.Quantum.Math.Complex) : Double
```


## <a name="input"></a>Eingabe

### <a name="input--complex"></a>Eingabe: [Komplex](xref:Microsoft.Quantum.Math.Complex)

Komplexe Zahl $c = x + i y $.



## <a name="output--double"></a>Ausgabe: [Double](xref:microsoft.quantum.lang-ref.double)

Absoluter Wert $ | c | = \sqrt{x ^ 2 + y ^ 2} $.