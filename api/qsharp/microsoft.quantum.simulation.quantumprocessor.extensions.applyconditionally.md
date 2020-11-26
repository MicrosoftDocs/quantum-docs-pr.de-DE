---
uid: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions.ApplyConditionally
title: Applybedingt-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions
qsharp.name: ApplyConditionally
qsharp.summary: ''
ms.openlocfilehash: 24d52576d2fb3e83f294874be4b0d1cd6a80f188
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96229068"
---
# <a name="applyconditionally-operation"></a>Applybedingt-Vorgang

Namespace: [Microsoft. Quantum. Simulation. quantumprocessor. Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)

Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)




```qsharp
operation ApplyConditionally<'T, 'U> (measurementResults : Result[], resultsValues : Result[], (onEqualOp : ('T => Unit), equalArg : 'T), (onNonEqualOp : ('U => Unit), nonEqualArg : 'U)) : Unit
```


## <a name="input"></a>Eingabe

### <a name="measurementresults--__invalidresult__"></a>"messrementresults": __ungültig <Result>__[]




### <a name="resultsvalues--__invalidresult__"></a>result values: __ungültig <Result>__[]




### <a name="onequalop--t--unit"></a>onequalop: 't => [Einheit](xref:microsoft.quantum.lang-ref.unit) 




### <a name="equalarg--t"></a>equalarg: 't




### <a name="onnonequalop--u--unit"></a>onnonequalop: ' U => [Einheit](xref:microsoft.quantum.lang-ref.unit) 




### <a name="nonequalarg--u"></a>nicht equalarg: "U





## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Typparameter

### <a name="t"></a>GIF


### <a name="u"></a>"U

