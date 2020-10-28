---
uid: Microsoft.Quantum.Arithmetic.SquareSI
title: Squaresi-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: SquareSI
qsharp.summary: Square signed integer `xs` and store the result in `result`, which must be zero initially.
ms.openlocfilehash: c8c4e3cca001aa6d7ce1b9df106ce77f74524301
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706218"
---
# <a name="squaresi-operation"></a>Squaresi-Vorgang

Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)

Paketen [](https://nuget.org/packages/)


Eine quadratische Ganzzahl `xs` mit Vorzeichen und speichert das Ergebnis in `result` , das anfänglich NULL sein muss.

```qsharp
operation SquareSI (xs : Microsoft.Quantum.Arithmetic.SignedLittleEndian, result : Microsoft.Quantum.Arithmetic.SignedLittleEndian) : Unit
```


## <a name="input"></a>Eingabe

### <a name="xs--signedlittleendian"></a>xs: [signedlittleenddian](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)

n-Bit-Ganzzahl in Quadrat (signedlittleendian)


### <a name="result--signedlittleendian"></a>Ergebnis: [signedlittleenddian](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)

Das 2N-Bit-Ergebnis (signedlittleendian) muss zunächst den Status $ \ket {0} $ aufweisen.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Hinweise

Die-Implementierung basiert auf integersquare.