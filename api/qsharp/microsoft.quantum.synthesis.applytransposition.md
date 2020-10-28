---
uid: Microsoft.Quantum.Synthesis.ApplyTransposition
title: Applytransformation-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: ApplyTransposition
qsharp.summary: ''
ms.openlocfilehash: 1bd6f9580e09752f1de75927d6bb35417bb1ff21
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92725258"
---
# <a name="applytransposition-operation"></a>Applytransformation-Vorgang

Namespace: [Microsoft. Quantum. Synthese](xref:Microsoft.Quantum.Synthesis)

Paketen [](https://nuget.org/packages/)




```qsharp
operation ApplyTransposition (a : Int, b : Int, qubits : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
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

