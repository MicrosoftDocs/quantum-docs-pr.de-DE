---
uid: Microsoft.Quantum.Canon.ApplyControlledOnBitString
title: Applycontrolledonbitstring-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyControlledOnBitString
qsharp.summary: Applies a unitary operation on the target register, controlled on a a state specified by a given bit mask.
ms.openlocfilehash: 82adc74e23e1d50cb6436176a973fdd1a0eeb3bd
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841947"
---
# <a name="applycontrolledonbitstring-operation"></a>Applycontrolledonbitstring-Vorgang

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Wendet einen einheitlichen Vorgang für das Ziel Register an, der in einem durch eine bestimmte Bitmaske angegebenen Zustand gesteuert wird.

```qsharp
operation ApplyControlledOnBitString<'T> (bits : Bool[], oracle : ('T => Unit is Adj + Ctl), controlRegister : Qubit[], targetRegister : 'T) : Unit is Adj + Ctl
```


## <a name="input"></a>Eingabe

### <a name="bits--bool"></a>Bits: [bool](xref:microsoft.quantum.lang-ref.bool)[]

Die Bitzeichenfolge, für die der angegebene einheitliche Vorgang gesteuert werden soll.


### <a name="oracle--t--unit--is-adj--ctl"></a>Oracle: 't => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL

Der auf das Ziel Register anzuwendende einheitliche Vorgang.


### <a name="controlregister--qubit"></a>controlregister: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Ein Quantum-Register, das die Anwendung von steuert `oracle` .


### <a name="targetregister--t"></a>targetregiester: 't

Das Ziel Register, das an als Eingabe an die übermittelt werden soll `oracle` .



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Typparameter

### <a name="t"></a>GIF



## <a name="remarks"></a>Bemerkungen

Das von angegebene Muster `bits` ist möglicherweise kürzer als `controlRegister` . in diesem Fall werden zusätzliche Steuerungs-Qubits ignoriert (d. h., Sie werden nicht für "$ \ket {0} $" und "$ \ket $" gesteuert {1} ).
Wenn `bits` länger als ist `controlRegister` , wird ein Fehler ausgelöst.

Beispielsweise `bits = [0,1,0,0,1]` bedeutet, dass `oracle` nur dann angewendet wird, wenn `controlRegister` sich im Zustand $ \ket {0} \ket {1} \ket \ket {0} {0} \ket {1} $ befindet.