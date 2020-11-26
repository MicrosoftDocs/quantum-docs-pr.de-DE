---
uid: Microsoft.Quantum.Arithmetic.ApplyPhaseLEOperationOnLE
title: Applyphaseleoperationonle-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyPhaseLEOperationOnLE
qsharp.summary: Applies an operation that takes a <xref:microsoft.quantum.arithmetic.littleendian> register as input on a target register of type <xref:microsoft.quantum.arithmetic.phaselittleendian>.
ms.openlocfilehash: adccad53e8d874cb2879d7005711624bbcc69201
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96190767"
---
# <a name="applyphaseleoperationonle-operation"></a>Applyphaseleoperationonle-Vorgang

Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Wendet einen Vorgang an, <xref:microsoft.quantum.arithmetic.littleendian> der ein Register als Eingabe für ein Ziel Register des Typs annimmt <xref:microsoft.quantum.arithmetic.phaselittleendian> .

```qsharp
operation ApplyPhaseLEOperationOnLE (op : (Microsoft.Quantum.Arithmetic.PhaseLittleEndian => Unit), target : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="input"></a>Eingabe

### <a name="op--phaselittleendian--unit"></a>OP: [phaselittleerdian](xref:Microsoft.Quantum.Arithmetic.PhaseLittleEndian) - => [Einheit](xref:microsoft.quantum.lang-ref.unit) 

Der anzuwendende Vorgang.


### <a name="target--littleendian"></a>Ziel: [littleenddian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Das Register, auf das der Vorgang angewendet wird.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Bemerkungen

Das Register wird `PhaseLittleEndian` durch die Verwendung von transformiert <xref:microsoft.quantum.canon.qftle> und dann nach der Anwendung von an seine ursprüngliche Darstellung zurückgegeben `op` .

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Canon. applyphaseleoperationonlea](xref:Microsoft.Quantum.Canon.ApplyPhaseLEOperationonLEA)
- [Microsoft. Quantum. Canon. applyphaseleoperationonlea](xref:Microsoft.Quantum.Canon.ApplyPhaseLEOperationonLEA)
- [Microsoft. Quantum. Canon. applyphaseleoperationonleca](xref:Microsoft.Quantum.Canon.ApplyPhaseLEOperationonLECA)