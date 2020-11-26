---
uid: Microsoft.Quantum.Math.AbsSquaredComplexPolar
title: Abssquaredcomplexpolar-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: AbsSquaredComplexPolar
qsharp.summary: Returns the squared absolute value of a complex number of type `ComplexPolar`.
ms.openlocfilehash: 51ec302d5120b2af58c00fc20c5c8cf739f189b1
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96211286"
---
# <a name="abssquaredcomplexpolar-function"></a>Abssquaredcomplexpolar-Funktion

Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Gibt den quadratischen absoluten Wert einer komplexen Zahl vom Typ zurück `ComplexPolar` .

```qsharp
function AbsSquaredComplexPolar (input : Microsoft.Quantum.Math.ComplexPolar) : Double
```


## <a name="input"></a>Eingabe

### <a name="input--complexpolar"></a>Eingabe: [complexpolar](xref:Microsoft.Quantum.Math.ComplexPolar)

Komplexe Zahl $c = r e ^ {i t} $.



## <a name="output--double"></a>Ausgabe: [Double](xref:microsoft.quantum.lang-ref.double)

Der absolute Wert $ | c | ^ 2 = r ^ 2 $ wird quadriert.