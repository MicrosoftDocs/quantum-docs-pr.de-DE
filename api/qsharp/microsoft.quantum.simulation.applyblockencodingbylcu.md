---
uid: Microsoft.Quantum.Simulation.ApplyBlockEncodingByLCU
title: Applyblockencodingbylcu-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: ApplyBlockEncodingByLCU
qsharp.summary: Implementation of `BlockEncodingByLCU`.
ms.openlocfilehash: 8ce6eb16b1dc5a83dd3a9559592c20d6b7b999b6
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96225481"
---
# <a name="applyblockencodingbylcu-operation"></a>Applyblockencodingbylcu-Vorgang

Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Implementierung von `BlockEncodingByLCU`.

```qsharp
operation ApplyBlockEncodingByLCU<'T, 'S> (statePreparation : ('T => Unit is Adj + Ctl), selector : (('T, 'S) => Unit is Adj + Ctl), auxiliary : 'T, system : 'S) : Unit is Adj + Ctl
```


## <a name="input"></a>Eingabe

### <a name="statepreparation--t--unit--is-adj--ctl"></a>statepreparation: 't => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL




### <a name="selector--ts--unit--is-adj--ctl"></a>Selektor: ('t, es) => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL




### <a name="auxiliary--t"></a>Zusatz: 't




### <a name="system--s"></a>System:





## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Typparameter

### <a name="t"></a>GIF


### <a name="s"></a>Spaniens

