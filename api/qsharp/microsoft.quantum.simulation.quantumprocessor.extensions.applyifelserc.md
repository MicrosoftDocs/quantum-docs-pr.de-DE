---
uid: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions.ApplyIfElseRC
title: Applyifelserc-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions
qsharp.name: ApplyIfElseRC
qsharp.summary: ''
ms.openlocfilehash: 21069c43c16bc9712973ac4e0afea8320c0d83a9
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92701250"
---
# <a name="applyifelserc-operation"></a>Applyifelserc-Vorgang

Namespace: [Microsoft. Quantum. Simulation. quantumprocessor. Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)

Paketen [](https://nuget.org/packages/)




```qsharp
operation ApplyIfElseRC<'T, 'U> (measurementResult : Result, (onResultZeroOp : ('T => Unit is Ctl), zeroArg : 'T), (onResultOneOp : ('U => Unit is Ctl), oneArg : 'U)) : Unit
```


## <a name="input"></a>Eingabe

### <a name="measurementresult--__invalidresult__"></a>messrementresult: __ungültig <Result>__




### <a name="onresultzeroop--t--unit-ctl"></a>onresultzeroop: 't => [Unit](xref:microsoft.quantum.lang-ref.unit) CTL




### <a name="zeroarg--t"></a>NULL: nicht




### <a name="onresultoneop--u--unit-ctl"></a>onresultoneop: "U => [Unit](xref:microsoft.quantum.lang-ref.unit) CTL




### <a name="onearg--u"></a>onearg: "U





## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Typparameter

### <a name="t"></a>GIF


### <a name="u"></a>"U

