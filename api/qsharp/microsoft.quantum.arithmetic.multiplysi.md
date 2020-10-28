---
uid: Microsoft.Quantum.Arithmetic.MultiplySI
title: Multiplysi-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: MultiplySI
qsharp.summary: Multiply signed integer `xs` by signed integer `ys` and store the result in `result`, which must be zero initially.
ms.openlocfilehash: 9ca781cbe90a8ec13e6a85a5babaf043bc8f2b5b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706362"
---
# <a name="multiplysi-operation"></a>Multiplysi-Vorgang

Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)

Paketen [](https://nuget.org/packages/)


Multiplizieren Sie eine ganze Zahl `xs` mit Vorzeichen `ys` , und speichern Sie das Ergebnis in `result` , das anfänglich NULL sein muss.

```qsharp
operation MultiplySI (xs : Microsoft.Quantum.Arithmetic.SignedLittleEndian, ys : Microsoft.Quantum.Arithmetic.SignedLittleEndian, result : Microsoft.Quantum.Arithmetic.SignedLittleEndian) : Unit
```


## <a name="input"></a>Eingabe

### <a name="xs--signedlittleendian"></a>xs: [signedlittleenddian](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)

n-Bit Multiplikand (signedlittleendian)


### <a name="ys--signedlittleendian"></a>YS: [signedlittleenddian](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)

n-Bit-Multiplikator (signedlittleendian)


### <a name="result--signedlittleendian"></a>Ergebnis: [signedlittleenddian](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)

Das 2N-Bit-Ergebnis (signedlittleendian) muss zunächst den Status $ \ket {0} $ aufweisen.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)

