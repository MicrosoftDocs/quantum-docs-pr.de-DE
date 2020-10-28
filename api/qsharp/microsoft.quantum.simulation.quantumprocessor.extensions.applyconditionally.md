---
uid: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions.ApplyConditionally
title: Applybedingt-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions
qsharp.name: ApplyConditionally
qsharp.summary: ''
ms.openlocfilehash: fe623b240e35ee88f673b6e90db6307ef701d049
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92701711"
---
# <a name="applyconditionally-operation"></a>Applybedingt-Vorgang

Namespace: [Microsoft. Quantum. Simulation. quantumprocessor. Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)

Paketen [](https://nuget.org/packages/)




```qsharp
operation ApplyConditionally<'T, 'U> (measurementResults : Result[], resultsValues : Result[], (onEqualOp : ('T => Unit), equalArg : 'T), (onNonEqualOp : ('U => Unit), nonEqualArg : 'U)) : Unit
```


## <a name="input"></a>Eingabe

### <a name="measurementresults--__invalidresult__"></a>"messrementresults": __ungültig <Result>__ []




### <a name="resultsvalues--__invalidresult__"></a>result values: __ungültig <Result>__ []




### <a name="onequalop--t--unit"></a>onequalop: 't => [Einheit](xref:microsoft.quantum.lang-ref.unit) 




### <a name="equalarg--t"></a>equalarg: 't




### <a name="onnonequalop--u--unit"></a>onnonequalop: ' U => [Einheit](xref:microsoft.quantum.lang-ref.unit) 




### <a name="nonequalarg--u"></a>nicht equalarg: "U





## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Typparameter

### <a name="t"></a>GIF


### <a name="u"></a>"U

