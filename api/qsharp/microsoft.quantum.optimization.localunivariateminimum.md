---
uid: Microsoft.Quantum.Optimization.LocalUnivariateMinimum
title: Localunivariateminimum-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Optimization
qsharp.name: LocalUnivariateMinimum
qsharp.summary: Returns the local minimum for a univariate function over a bounded interval, using a golden interval search.
ms.openlocfilehash: e804e6a6ed82f14dcc9b8f721ad503d77922dc0f
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96194082"
---
# <a name="localunivariateminimum-function"></a>Localunivariateminimum-Funktion

Namespace: [Microsoft. Quantum. Optimization](xref:Microsoft.Quantum.Optimization)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Gibt das lokale Minimum für eine Univariate-Funktion über ein begrenztes Intervall zurück, wobei eine Golden Interval-Suche verwendet wird.

```qsharp
function LocalUnivariateMinimum (fn : (Double -> Double), bounds : (Double, Double), tolerance : Double) : Microsoft.Quantum.Optimization.UnivariateOptimizationResult
```


## <a name="input"></a>Eingabe

### <a name="fn--double---double"></a>FN: [Double](xref:microsoft.quantum.lang-ref.double) -> [Double](xref:microsoft.quantum.lang-ref.double)

Die Univariate-Funktion, die minimiert werden soll.


### <a name="bounds--doubledouble"></a>Begrenzungen: ([Double](xref:microsoft.quantum.lang-ref.double),[Double](xref:microsoft.quantum.lang-ref.double))

Das Intervall, in dem das lokale Minimum zu finden ist.


### <a name="tolerance--double"></a>Toleranz: [Double](xref:microsoft.quantum.lang-ref.double)

Die Genauigkeit in der zu tolerier enden Funktions Eingabe.
Die Suche nach lokalem Optima wird fortgesetzt, bis das Intervall kleiner als diese Toleranz ist.



## <a name="output--univariateoptimizationresult"></a>Ausgabe: [univariateoptimizationresult](xref:Microsoft.Quantum.Optimization.UnivariateOptimizationResult)

Ein lokaler Optima der angegebenen Funktion, der sich innerhalb der angegebenen Begrenzungen befindet.