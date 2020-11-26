---
uid: Microsoft.Quantum.Optimization.UnivariateOptimizationResult
title: Benutzerdefinierter univariateoptimizationresult-Typ
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Optimization
qsharp.name: UnivariateOptimizationResult
qsharp.summary: Represents the result of optimizing a univariate function.
ms.openlocfilehash: 0bcdbda5586181f965297cb2a398d766f9c6fabb
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96194031"
---
# <a name="univariateoptimizationresult-user-defined-type"></a>Benutzerdefinierter univariateoptimizationresult-Typ

Namespace: [Microsoft. Quantum. Optimization](xref:Microsoft.Quantum.Optimization)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Stellt das Ergebnis der Optimierung einer Univariate-Funktion dar.

```qsharp

newtype UnivariateOptimizationResult = (Coordinate : Double, Value : Double);
```



## <a name="named-items"></a>Benannte Elemente

### <a name="coordinate--double"></a>Koordinate: [Double](xref:microsoft.quantum.lang-ref.double)

Eingabe, bei der eine optimale gefunden wurde.
### <a name="value--double"></a>Wert: [Double](xref:microsoft.quantum.lang-ref.double)

Der Wert, der von der Funktion beim optimalen Wert zurückgegeben wird.