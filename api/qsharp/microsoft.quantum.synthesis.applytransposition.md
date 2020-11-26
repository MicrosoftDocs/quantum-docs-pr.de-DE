---
uid: Microsoft.Quantum.Synthesis.ApplyTransposition
title: Applytransformation-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: ApplyTransposition
qsharp.summary: ''
ms.openlocfilehash: ca22b090f2b2613f07caef698941ea608374ab1e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96203313"
---
# <a name="applytransposition-operation"></a>Applytransformation-Vorgang

Namespace: [Microsoft. Quantum. Synthese](xref:Microsoft.Quantum.Synthesis)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)




```qsharp
operation ApplyTransposition (a : Int, b : Int, qubits : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a>BESCHREIBUNG

Mit diesem Vorgang wird die Amplitude beim Index `a` mit der Amplitude bei Index `b` im angegebenen Status Vektor der `register` Länge $n $ vertauscht.  Wenn `a` entspricht `b` , wird der Zustands Vektor nicht geändert.

## <a name="input"></a>Eingabe

### <a name="a--int"></a>a: [int](xref:microsoft.quantum.lang-ref.int)

Erster Index (muss ein Wert zwischen 0 und $2 ^ n-$1 sein)


### <a name="b--int"></a>b: [int](xref:microsoft.quantum.lang-ref.int)

Zweiter Index (muss ein Wert zwischen 0 und $2 ^ n-$1 sein)


### <a name="qubits--littleendian"></a>Qubits: [littleenddian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Eine Liste von $n $ Qubits, auf die die-Umsetzung angewendet wird.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)

