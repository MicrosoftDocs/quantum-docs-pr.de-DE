---
uid: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions.ApplyConditionallyCA
title: Applyconditionallyca-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions
qsharp.name: ApplyConditionallyCA
qsharp.summary: ''
ms.openlocfilehash: e456ed5d8f7f17a914401473948c89c020174903
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706647"
---
# <a name="applyconditionallyca-operation"></a>Applyconditionallyca-Vorgang

Namespace: [Microsoft. Quantum. Simulation. quantumprocessor. Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)

Paketen [](https://nuget.org/packages/)




```qsharp
operation ApplyConditionallyCA<'T, 'U> (measurementResults : Result[], resultsValues : Result[], (onEqualOp : ('T => Unit is Ctl + Adj), equalArg : 'T), (onNonEqualOp : ('U => Unit is Ctl + Adj), nonEqualArg : 'U)) : Unit
```


## <a name="input"></a>Eingabe

### <a name="measurementresults--__invalidresult__"></a>"messrementresults": __ungültig <Result>__ []




### <a name="resultsvalues--__invalidresult__"></a>result values: __ungültig <Result>__ []




### <a name="onequalop--t--unit-ctl--adj"></a>onequalop: 't => [Unit](xref:microsoft.quantum.lang-ref.unit) CTL + ADJ




### <a name="equalarg--t"></a>equalarg: 't




### <a name="onnonequalop--u--unit-ctl--adj"></a>onnonequalop: ' U => [Unit](xref:microsoft.quantum.lang-ref.unit) CTL + ADJ




### <a name="nonequalarg--u"></a>nicht equalarg: "U





## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Typparameter

### <a name="t"></a>GIF


### <a name="u"></a>"U

