---
uid: Microsoft.Quantum.Canon.MultiplexOperationsWithAuxRegister
title: Multiplexoperationswithauxregister-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: MultiplexOperationsWithAuxRegister
qsharp.summary: Implementation step of MultiplexOperations.
ms.openlocfilehash: f6a90657324f8528aaa2e9e511a7f8cbcd2f540f
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703962"
---
# <a name="multiplexoperationswithauxregister-operation"></a>Multiplexoperationswithauxregister-Vorgang

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paketen [](https://nuget.org/packages/)


Implementierungs Schritt von multiplexoperations.

```qsharp
operation MultiplexOperationsWithAuxRegister<'T> (unitaries : ('T => Unit is Adj + Ctl)[], auxillaryRegister : Qubit[], index : Microsoft.Quantum.Arithmetic.LittleEndian, target : 'T) : Unit
```


## <a name="input"></a>Eingabe

### <a name="unitaries--t--unit-adj--ctl"></a>Uni-Zuflüsse: 't => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL []




### <a name="auxillaryregister--qubit"></a>"auxillaryregister": [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]




### <a name="index--littleendian"></a>Index: [littleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)




### <a name="target--t"></a>Ziel: 't





## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Typparameter

### <a name="t"></a>GIF



## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Canon. multiplexoperations](xref:Microsoft.Quantum.Canon.MultiplexOperations)