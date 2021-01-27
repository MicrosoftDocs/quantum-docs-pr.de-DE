---
uid: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions.ApplyConditionallyC
title: Applyconditionallyc-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions
qsharp.name: ApplyConditionallyC
qsharp.summary: ''
ms.openlocfilehash: 09496d384a70fa9fb6826304ce9909034297a118
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98847850"
---
# <a name="applyconditionallyc-operation"></a>Applyconditionallyc-Vorgang

Namespace: [Microsoft. Quantum. Simulation. quantumprocessor. Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)

Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)




```qsharp
operation ApplyConditionallyC<'T, 'U> (measurementResults : Result[], resultsValues : Result[], (onEqualOp : ('T => Unit is Ctl), equalArg : 'T), (onNonEqualOp : ('U => Unit is Ctl), nonEqualArg : 'U)) : Unit is Ctl
```


## <a name="input"></a>Eingabe

### <a name="measurementresults--__invalidresult__"></a>"messrementresults": __ungültig <Result>__[]




### <a name="resultsvalues--__invalidresult__"></a>result values: __ungültig <Result>__[]




### <a name="onequalop--t--unit--is-ctl"></a>onequalop: 't => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist CTL




### <a name="equalarg--t"></a>equalarg: 't




### <a name="onnonequalop--u--unit--is-ctl"></a>onnonequalop: "U => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist CTL




### <a name="nonequalarg--u"></a>nicht equalarg: "U





## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Typparameter

### <a name="t"></a>GIF


### <a name="u"></a>"U

