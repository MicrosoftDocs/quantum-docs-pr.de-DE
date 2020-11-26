---
uid: Microsoft.Quantum.Canon.ControlledOnInt
title: Controlledonint-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ControlledOnInt
qsharp.summary: Returns a unitary operator that applies an oracle on the target register if the control register state corresponds to a specified positive integer.
ms.openlocfilehash: 3cc5c00d9c7295106901149e06571ef1963d1323
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96207257"
---
# <a name="controlledonint-function"></a>Controlledonint-Funktion

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Gibt einen einheitlichen Operator zurück, der ein Oracle auf das Ziel Register anwendet, wenn der Steuerelement Registrierungs Zustand einer angegebenen positiven ganzen Zahl entspricht.

```qsharp
function ControlledOnInt<'T> (numberState : Int, oracle : ('T => Unit is Adj + Ctl)) : ((Qubit[], 'T) => Unit is Adj + Ctl)
```


## <a name="input"></a>Eingabe

### <a name="numberstate--int"></a>numstate: [int](xref:microsoft.quantum.lang-ref.int)

Positive Ganzzahl.


### <a name="oracle--t--unit--is-adj--ctl"></a>Oracle: 't => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL

Einheitlicher Operator.



## <a name="output--qubitt--unit--is-adj--ctl"></a>Ausgabe: ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[], 't) => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL

Ein einheitlicher Operator, `oracle` der auf das Ziel Register angewendet wird, wenn der Registrierungs Zustand des Steuer Elements dem Zahlen Zustand entspricht `numberState` .

## <a name="type-parameters"></a>Typparameter

### <a name="t"></a>GIF



## <a name="remarks"></a>Bemerkungen

Der Wert von `numberState` wird mithilfe einer Little-enumdian-Codierung interpretiert.