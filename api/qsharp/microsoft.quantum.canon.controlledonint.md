---
uid: Microsoft.Quantum.Canon.ControlledOnInt
title: Controlledonint-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ControlledOnInt
qsharp.summary: Returns a unitary operator that applies an oracle on the target register if the control register state corresponds to a specified positive integer.
ms.openlocfilehash: 4c48f3257f91fc50040d02cae7c2f7bdf87ea7c5
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704311"
---
# <a name="controlledonint-function"></a>Controlledonint-Funktion

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paketen [](https://nuget.org/packages/)


Gibt einen einheitlichen Operator zurück, der ein Oracle auf das Ziel Register anwendet, wenn der Steuerelement Registrierungs Zustand einer angegebenen positiven ganzen Zahl entspricht.

```qsharp
function ControlledOnInt<'T> (numberState : Int, oracle : ('T => Unit is Adj + Ctl)) : ((Qubit[], 'T) => Unit is Adj + Ctl)
```


## <a name="input"></a>Eingabe

### <a name="numberstate--int"></a>numstate: [int](xref:microsoft.quantum.lang-ref.int)

Positive Ganzzahl.


### <a name="oracle--t--unit-adj--ctl"></a>Oracle: 't => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL

Einheitlicher Operator.



## <a name="output--qubitt--unit-adj--ctl"></a>Ausgabe: ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[], 't) => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL

Ein einheitlicher Operator, `oracle` der auf das Ziel Register angewendet wird, wenn der Registrierungs Zustand des Steuer Elements dem Zahlen Zustand entspricht `numberState` .

## <a name="type-parameters"></a>Typparameter

### <a name="t"></a>GIF



## <a name="remarks"></a>Hinweise

Der Wert von `numberState` wird mithilfe einer Little-enumdian-Codierung interpretiert.