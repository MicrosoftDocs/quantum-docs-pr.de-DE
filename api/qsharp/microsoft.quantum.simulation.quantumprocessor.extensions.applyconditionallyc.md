---
uid: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions.ApplyConditionallyC
title: Applyconditionallyc-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions
qsharp.name: ApplyConditionallyC
qsharp.summary: ''
ms.openlocfilehash: fc1cf50b7befd40cf20720032329438715a9b856
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706655"
---
# <a name="applyconditionallyc-operation"></a>Applyconditionallyc-Vorgang

Namespace: [Microsoft. Quantum. Simulation. quantumprocessor. Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)

Paketen [](https://nuget.org/packages/)




```qsharp
operation ApplyConditionallyC<'T, 'U> (measurementResults : Result[], resultsValues : Result[], (onEqualOp : ('T => Unit is Ctl), equalArg : 'T), (onNonEqualOp : ('U => Unit is Ctl), nonEqualArg : 'U)) : Unit
```


## <a name="input"></a>Eingabe

### <a name="measurementresults--__invalidresult__"></a>"messrementresults": __ungültig <Result>__ []




### <a name="resultsvalues--__invalidresult__"></a>result values: __ungültig <Result>__ []




### <a name="onequalop--t--unit-ctl"></a>onequalop: 't => [Unit](xref:microsoft.quantum.lang-ref.unit) CTL




### <a name="equalarg--t"></a>equalarg: 't




### <a name="onnonequalop--u--unit-ctl"></a>onnonequalop: "U => [Unit](xref:microsoft.quantum.lang-ref.unit) CTL




### <a name="nonequalarg--u"></a>nicht equalarg: "U





## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Typparameter

### <a name="t"></a>GIF


### <a name="u"></a>"U

