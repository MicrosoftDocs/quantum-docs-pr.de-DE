---
uid: Microsoft.Quantum.Optimization.LocalUnivariateMinimum
title: Localunivariateminimum-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Optimization
qsharp.name: LocalUnivariateMinimum
qsharp.summary: Returns the local minimum for a univariate function over a bounded interval, using a golden interval search.
ms.openlocfilehash: 3b09af88bbed20a392768d005e5e9567b3bb7022
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92701916"
---
# <a name="localunivariateminimum-function"></a>Localunivariateminimum-Funktion

Namespace: [Microsoft. Quantum. Optimization](xref:Microsoft.Quantum.Optimization)

Paketen [](https://nuget.org/packages/)


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