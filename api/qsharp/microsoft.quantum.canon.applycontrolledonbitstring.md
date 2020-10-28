---
uid: Microsoft.Quantum.Canon.ApplyControlledOnBitString
title: Applycontrolledonbitstring-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyControlledOnBitString
qsharp.summary: Applies a unitary operation on the target register, controlled on a a state specified by a given bit mask.
ms.openlocfilehash: 7a054511bacff574e6f7e889ace048c78886cf91
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705434"
---
# <a name="applycontrolledonbitstring-operation"></a>Applycontrolledonbitstring-Vorgang

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paketen [](https://nuget.org/packages/)


Wendet einen einheitlichen Vorgang für das Ziel Register an, der in einem durch eine bestimmte Bitmaske angegebenen Zustand gesteuert wird.

```qsharp
operation ApplyControlledOnBitString<'T> (bits : Bool[], oracle : ('T => Unit is Adj + Ctl), controlRegister : Qubit[], targetRegister : 'T) : Unit
```


## <a name="input"></a>Eingabe

### <a name="bits--bool"></a>Bits: [bool](xref:microsoft.quantum.lang-ref.bool)[]

Die Bitzeichenfolge, für die der angegebene einheitliche Vorgang gesteuert werden soll.


### <a name="oracle--t--unit-adj--ctl"></a>Oracle: 't => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL

Der auf das Ziel Register anzuwendende einheitliche Vorgang.


### <a name="controlregister--qubit"></a>controlregister: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Ein Quantum-Register, das die Anwendung von steuert `oracle` .


### <a name="targetregister--t"></a>targetregiester: 't

Das Ziel Register, das an als Eingabe an die übermittelt werden soll `oracle` .



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Typparameter

### <a name="t"></a>GIF



## <a name="remarks"></a>Hinweise

Das von angegebene Muster `bits` ist möglicherweise kürzer als `controlRegister` . in diesem Fall werden zusätzliche Steuerungs-Qubits ignoriert (d. h., Sie werden nicht für "$ \ket {0} $" und "$ \ket $" gesteuert {1} ).
Wenn `bits` länger als ist `controlRegister` , wird ein Fehler ausgelöst.

Beispielsweise `bits = [0,1,0,0,1]` bedeutet, dass `oracle` nur dann angewendet wird, wenn `controlRegister` sich im Zustand $ \ket {0} \ket {1} \ket \ket {0} {0} \ket {1} $ befindet.