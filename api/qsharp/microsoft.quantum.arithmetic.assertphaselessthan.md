---
uid: Microsoft.Quantum.Arithmetic.AssertPhaseLessThan
title: Assertphas;than-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: AssertPhaseLessThan
qsharp.summary: Asserts that the `number` encoded in PhaseLittleEndian is less than `value`.
ms.openlocfilehash: d003d83a84356ce52c5601135000813c7f119e4d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707447"
---
# <a name="assertphaselessthan-operation"></a>Assertphas;than-Vorgang

Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)

Paketen [](https://nuget.org/packages/)


Bestätigt, dass der `number` codierte in phaselittleenddian kleiner als ist `value` .

```qsharp
operation AssertPhaseLessThan (value : Int, number : Microsoft.Quantum.Arithmetic.PhaseLittleEndian) : Unit
```


## <a name="input"></a>Eingabe

### <a name="value--int"></a>Wert: [int](xref:microsoft.quantum.lang-ref.int)

`number` muss kleiner sein als.


### <a name="number--phaselittleendian"></a>Zahl: [phaselittleddian](xref:Microsoft.Quantum.Arithmetic.PhaseLittleEndian)

Ganzzahl ohne Vorzeichen, die mit verglichen wird `value` .



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Hinweise

Von der kontrollierten Version dieses Vorgangs werden Steuerelemente ignoriert.