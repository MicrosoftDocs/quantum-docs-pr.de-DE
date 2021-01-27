---
uid: Microsoft.Quantum.Arithmetic.MultiplySI
title: Multiplysi-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: MultiplySI
qsharp.summary: Multiply signed integer `xs` by signed integer `ys` and store the result in `result`, which must be zero initially.
ms.openlocfilehash: 7c7e7dfaee9b9dc717db44956506984e60281dd2
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843011"
---
# <a name="multiplysi-operation"></a>Multiplysi-Vorgang

Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)

Paket: [Microsoft. Quantum. Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)


Multiplizieren Sie eine ganze Zahl `xs` mit Vorzeichen `ys` , und speichern Sie das Ergebnis in `result` , das anfänglich NULL sein muss.

```qsharp
operation MultiplySI (xs : Microsoft.Quantum.Arithmetic.SignedLittleEndian, ys : Microsoft.Quantum.Arithmetic.SignedLittleEndian, result : Microsoft.Quantum.Arithmetic.SignedLittleEndian) : Unit is Adj + Ctl
```


## <a name="input"></a>Eingabe

### <a name="xs--signedlittleendian"></a>xs: [signedlittleenddian](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)

n-Bit Multiplikand (signedlittleendian)


### <a name="ys--signedlittleendian"></a>YS: [signedlittleenddian](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)

n-Bit-Multiplikator (signedlittleendian)


### <a name="result--signedlittleendian"></a>Ergebnis: [signedlittleenddian](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)

Das 2N-Bit-Ergebnis (signedlittleendian) muss zunächst den Status $ \ket {0} $ aufweisen.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)

