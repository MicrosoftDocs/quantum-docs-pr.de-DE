---
uid: Microsoft.Quantum.Arithmetic.AddI
title: ADDI-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: AddI
qsharp.summary: Automatically chooses between addition with carry and without, depending on the register size of `ys`.
ms.openlocfilehash: 9a90d15defd57cf2836a6fda5b52ddaa816fd55e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96191022"
---
# <a name="addi-operation"></a>ADDI-Vorgang

Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)

Paket: [Microsoft. Quantum. Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)


Wählt in Abhängigkeit von der Register Größe von automatisch zwischen Addition und ohne ausführen und ohne aus `ys` .

```qsharp
operation AddI (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="input"></a>Eingabe

### <a name="xs--littleendian"></a>xs: [littleenddian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

$n $-Bit-Addend.


### <a name="ys--littleendian"></a>YS: [littleumdian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Addend mit mindestens $n $ Qubits. Enthält das Ergebnis.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)

