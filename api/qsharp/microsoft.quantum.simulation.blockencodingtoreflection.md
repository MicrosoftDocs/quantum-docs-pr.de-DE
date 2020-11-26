---
uid: Microsoft.Quantum.Simulation.BlockEncodingToReflection
title: Blockencodingtoreflection-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: BlockEncodingToReflection
qsharp.summary: >-
  Converts a `BlockEncoding` into an equivalent `BLockEncodingReflection`.

  That is, given a `BlockEncoding` unitary $U$ that encodes some operator $H$ of interest, converts it into a `BlockEncodingReflection` $U'$ that encodes the same operator, but also satisfies $U'^\dagger = U'$. This increases the size of the auxiliary register of $U$ by one qubit.
ms.openlocfilehash: 742d4f5623c7c26810998f6c96e2c7b05cc452d3
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96225345"
---
# <a name="blockencodingtoreflection-function"></a>Blockencodingtoreflection-Funktion

Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


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

## <a name="remarks"></a>Bemerkungen

Dadurch wird die Größe des zusätzlichen Registers $U $ um ein Qubit vergrößert.

## <a name="references"></a>Referenzen

- Hamiltona Simulation by qubitisierung Guang Hao Low, ISAL. Chuang https://arxiv.org/abs/1610.06546

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Simulation. blockencoding](xref:Microsoft.Quantum.Simulation.BlockEncoding)
- [Microsoft. Quantum. Simulation. blockencodingreflection](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection)