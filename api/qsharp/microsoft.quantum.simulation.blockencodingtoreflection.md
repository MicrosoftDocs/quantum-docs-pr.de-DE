---
uid: Microsoft.Quantum.Simulation.BlockEncodingToReflection
title: Blockencodingtoreflection-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: BlockEncodingToReflection
qsharp.summary: >-
  Converts a `BlockEncoding` into an equivalent `BLockEncodingReflection`.

  That is, given a `BlockEncoding` unitary $U$ that encodes some operator $H$ of interest, converts it into a `BlockEncodingReflection` $U'$ that encodes the same operator, but also satisfies $U'^\dagger = U'$. This increases the size of the auxiliary register of $U$ by one qubit.
ms.openlocfilehash: a8b4c65f8c32f7f9185f1dbdacf8fc75fd4573b1
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92722066"
---
# <a name="blockencodingtoreflection-function"></a>Blockencodingtoreflection-Funktion

Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)

Paketen [](https://nuget.org/packages/)


Konvertiert einen `BlockEncoding` in eine-Entsprechung `BLockEncodingReflection` .

Das heißt, bei einem `BlockEncoding` einheitlichen $U $, der einen Operator $H $ of Interest codiert, konvertiert ihn in eine `BlockEncodingReflection` $U ' $, die denselben Operator codiert, aber auch $U ' ^ \dagger = U ' $ entspricht.
Dadurch wird die Größe des zusätzlichen Registers $U $ um ein Qubit vergrößert.

```qsharp
function BlockEncodingToReflection (blockEncoding : Microsoft.Quantum.Simulation.BlockEncoding) : Microsoft.Quantum.Simulation.BlockEncodingReflection
```


## <a name="input"></a>Eingabe

### <a name="blockencoding--blockencoding"></a>blockencoding: [blockencoding](xref:Microsoft.Quantum.Simulation.BlockEncoding)

Ein `BlockEncoding` einheitlicher $U $, der in eine Reflektion konvertiert werden soll.



## <a name="output--blockencodingreflection"></a>Ausgabe: [blockencodingreflection](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection)

Ein einheitlicher $U ' $, der sich zusammen für Register registriert `a` und `s` $H $ codiert und $U ' ^ \dagger = U ' $ entspricht.

## <a name="remarks"></a>Hinweise

Dadurch wird die Größe des zusätzlichen Registers $U $ um ein Qubit vergrößert.

## <a name="references"></a>Referenzen

- Hamiltona Simulation by qubitisierung Guang Hao Low, ISAL. Chuang https://arxiv.org/abs/1610.06546

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Simulation. blockencoding](xref:Microsoft.Quantum.Simulation.BlockEncoding)
- [Microsoft. Quantum. Simulation. blockencodingreflection](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection)