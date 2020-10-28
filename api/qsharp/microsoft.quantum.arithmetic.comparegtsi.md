---
uid: Microsoft.Quantum.Arithmetic.CompareGTSI
title: Comparegtsi-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: CompareGTSI
qsharp.summary: 'Wrapper for signed integer comparison: `result = xs > ys`.'
ms.openlocfilehash: 735ae21168d8efb3e626a8f1ea36e97f5cdf8760
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707383"
---
# <a name="comparegtsi-operation"></a>Comparegtsi-Vorgang

Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)

Paketen [](https://nuget.org/packages/)


Wrapper für ganzzahligen Vergleich mit Vorzeichen: `result = xs > ys` .

```qsharp
operation CompareGTSI (xs : Microsoft.Quantum.Arithmetic.SignedLittleEndian, ys : Microsoft.Quantum.Arithmetic.SignedLittleEndian, result : Qubit) : Unit
```


## <a name="input"></a>Eingabe

### <a name="xs--signedlittleendian"></a>xs: [signedlittleenddian](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)

Erste $n $-Bit-Nummer


### <a name="ys--signedlittleendian"></a>YS: [signedlittleenddian](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)

Sekunde $n $-Bit-Zahl


### <a name="result--qubit"></a>Ergebnis: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

Wird gekippt, wenn $XS > YS $



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)

