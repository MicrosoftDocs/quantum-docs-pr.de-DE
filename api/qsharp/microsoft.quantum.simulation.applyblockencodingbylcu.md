---
uid: Microsoft.Quantum.Simulation.ApplyBlockEncodingByLCU
title: Applyblockencodingbylcu-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: ApplyBlockEncodingByLCU
qsharp.summary: Implementation of `BlockEncodingByLCU`.
ms.openlocfilehash: 1575b93b6c3242e1dffafb330c44cc017a72a8b1
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92722122"
---
# <a name="applyblockencodingbylcu-operation"></a>Applyblockencodingbylcu-Vorgang

Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)

Paketen [](https://nuget.org/packages/)


Implementierung von `BlockEncodingByLCU`.

```qsharp
operation ApplyBlockEncodingByLCU<'T, 'S> (statePreparation : ('T => Unit is Adj + Ctl), selector : (('T, 'S) => Unit is Adj + Ctl), auxiliary : 'T, system : 'S) : Unit
```


## <a name="input"></a>Eingabe

### <a name="statepreparation--t--unit-adj--ctl"></a>statepreparation: 't => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL




### <a name="selector--ts--unit-adj--ctl"></a>Selektor: ('t, es) => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL




### <a name="auxiliary--t"></a>Zusatz: 't




### <a name="system--s"></a>System:





## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Typparameter

### <a name="t"></a>GIF


### <a name="s"></a>Spaniens

