---
uid: Microsoft.Quantum.Arithmetic.ApplyLEOperationOnPhaseLEA
title: Applyleoperationonphaselea-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyLEOperationOnPhaseLEA
qsharp.summary: Applies an operation that takes a <xref:microsoft.quantum.arithmetic.phaselittleendian> register as input on a target register of type <xref:microsoft.quantum.arithmetic.littleendian>.
ms.openlocfilehash: 408bd4e5d7146a74d7aec233765a63b2086b8ede
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96190852"
---
# <a name="applyleoperationonphaselea-operation"></a>Applyleoperationonphaselea-Vorgang

Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Wendet einen Vorgang an, <xref:microsoft.quantum.arithmetic.phaselittleendian> der ein Register als Eingabe für ein Ziel Register des Typs annimmt <xref:microsoft.quantum.arithmetic.littleendian> .

```qsharp
operation ApplyLEOperationOnPhaseLEA (op : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Adj), target : Microsoft.Quantum.Arithmetic.PhaseLittleEndian) : Unit is Adj
```


## <a name="input"></a>Eingabe

### <a name="op--littleendian--unit--is-adj"></a>OP: [littleandian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ

Der anzuwendende Vorgang.


### <a name="target--phaselittleendian"></a>Ziel: [phaselittleenddian](xref:Microsoft.Quantum.Arithmetic.PhaseLittleEndian)

Das Register, auf das der Vorgang angewendet wird.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Bemerkungen

Das Register wird `LittleEndian` durch die Verwendung von transformiert <xref:microsoft.quantum.canon.qftle> und dann nach der Anwendung von an seine ursprüngliche Darstellung zurückgegeben `op` .

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Canon. applyleoperationonphasele](xref:Microsoft.Quantum.Canon.ApplyLEOperationonPhaseLE)
- [Microsoft. Quantum. Canon. applyleoperationonphaselec](xref:Microsoft.Quantum.Canon.ApplyLEOperationonPhaseLEC)
- [Microsoft. Quantum. Canon. applyleoperationonphaseleca](xref:Microsoft.Quantum.Canon.ApplyLEOperationonPhaseLECA)