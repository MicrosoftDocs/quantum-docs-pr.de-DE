---
uid: Microsoft.Quantum.Canon.ApplyControlledOnInt
title: Applycontrolledonint-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyControlledOnInt
qsharp.summary: Applies a unitary operation on the target register if the control register state corresponds to a specified positive integer.
ms.openlocfilehash: 3dd17e6bc913e84941a6b81f134e60536a4c4122
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96219004"
---
# <a name="applycontrolledonint-operation"></a>Applycontrolledonint-Vorgang

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Wendet einen einheitlichen Vorgang auf das Ziel Register an, wenn der Steuerelement Registrierungs Zustand einer angegebenen positiven ganzen Zahl entspricht.

```qsharp
operation ApplyControlledOnInt<'T> (numberState : Int, oracle : ('T => Unit is Adj + Ctl), controlRegister : Qubit[], targetRegister : 'T) : Unit is Adj + Ctl
```


## <a name="input"></a>Eingabe

### <a name="numberstate--int"></a>numstate: [int](xref:microsoft.quantum.lang-ref.int)

Eine nicht negative ganze Zahl, für die der Vorgang `oracle` gesteuert werden soll.


### <a name="oracle--t--unit--is-adj--ctl"></a>Oracle: 't => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL

Ein einheitlicher Vorgang, der gesteuert werden soll.


### <a name="controlregister--qubit"></a>controlregister: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Ein Quantum-Register, das die Anwendung von steuert `oracle` .


### <a name="targetregister--t"></a>targetregiester: 't

Ein Register, das angewendet werden soll `oracle` .



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Typparameter

### <a name="t"></a>GIF



## <a name="remarks"></a>Bemerkungen

Der Wert von `numberState` wird mithilfe einer Little-enumdian-Codierung interpretiert.

`numberState` muss höchstens $2 ^ \texttt{length (controlregister)}-$1.
Beispielsweise `numberState = 537` bedeutet, dass `oracle` nur dann angewendet wird, wenn `controlRegister` sich im Zustand $ \ket {537} $ befindet.