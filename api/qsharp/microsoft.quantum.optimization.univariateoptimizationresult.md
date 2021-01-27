---
uid: Microsoft.Quantum.Optimization.UnivariateOptimizationResult
title: Benutzerdefinierter univariateoptimizationresult-Typ
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Optimization
qsharp.name: UnivariateOptimizationResult
qsharp.summary: Represents the result of optimizing a univariate function.
ms.openlocfilehash: cc54c0035796aac86482e8a3a6896ceb197c7cfe
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854568"
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