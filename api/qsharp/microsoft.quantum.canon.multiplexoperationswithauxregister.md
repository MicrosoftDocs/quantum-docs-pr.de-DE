---
uid: Microsoft.Quantum.Canon.MultiplexOperationsWithAuxRegister
title: Multiplexoperationswithauxregister-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: MultiplexOperationsWithAuxRegister
qsharp.summary: Implementation step of MultiplexOperations.
ms.openlocfilehash: 91db22d6261709c1c3506c80ff600c904748575a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98852461"
---
# <a name="multiplexoperationswithauxregister-operation"></a>Multiplexoperationswithauxregister-Vorgang

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Implementierungs Schritt von multiplexoperations.

```qsharp
operation MultiplexOperationsWithAuxRegister<'T> (unitaries : ('T => Unit is Adj + Ctl)[], auxillaryRegister : Qubit[], index : Microsoft.Quantum.Arithmetic.LittleEndian, target : 'T) : Unit is Adj + Ctl
```


## <a name="input"></a>Eingabe

### <a name="unitaries--t--unit--is-adj--ctl"></a>Uni-Zuflüsse: 't => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL []




### <a name="auxillaryregister--qubit"></a>"auxillaryregister": [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]




### <a name="index--littleendian"></a>Index: [littleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)




### <a name="target--t"></a>Ziel: 't





## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Typparameter

### <a name="t"></a>GIF



## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Canon. multiplexoperations](xref:Microsoft.Quantum.Canon.MultiplexOperations)