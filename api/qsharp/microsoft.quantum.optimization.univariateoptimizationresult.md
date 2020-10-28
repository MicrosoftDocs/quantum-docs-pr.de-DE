---
uid: Microsoft.Quantum.Optimization.UnivariateOptimizationResult
title: Benutzerdefinierter univariateoptimizationresult-Typ
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Optimization
qsharp.name: UnivariateOptimizationResult
qsharp.summary: Represents the result of optimizing a univariate function.
ms.openlocfilehash: c8aa91bbdc9e9e9bb4d110b470ff2041f9460a38
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92724320"
---
# <a name="univariateoptimizationresult-user-defined-type"></a>Benutzerdefinierter univariateoptimizationresult-Typ

Namespace: [Microsoft. Quantum. Optimization](xref:Microsoft.Quantum.Optimization)

Paketen [](https://nuget.org/packages/)


Stellt das Ergebnis der Optimierung einer Univariate-Funktion dar.

```qsharp

newtype UnivariateOptimizationResult = (Coordinate : Double, Value : Double);
```



## <a name="named-items"></a>Benannte Elemente

### <a name="coordinate--double"></a>Koordinate: [Double](xref:microsoft.quantum.lang-ref.double)

Eingabe, bei der eine optimale gefunden wurde.
### <a name="value--double"></a>Wert: [Double](xref:microsoft.quantum.lang-ref.double)

Der Wert, der von der Funktion beim optimalen Wert zurückgegeben wird.