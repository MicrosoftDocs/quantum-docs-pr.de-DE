---
uid: Microsoft.Quantum.Canon.EmbedPauli
title: Embedpauli-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: EmbedPauli
qsharp.summary: Given a single-qubit Pauli operator and the index of a qubit, returns a multi-qubit Pauli operator with the given single-qubit operator at that index and `PauliI` at every other index.
ms.openlocfilehash: c78406aa4557834ac2bb40cf1847696d075e5135
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704186"
---
# <a name="embedpauli-function"></a>Embedpauli-Funktion

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paketen [](https://nuget.org/packages/)


Gibt bei einem Single-Qubit-Pauli-Operator und dem Index eines Qubits einen multiqubit-Pauli-Operator mit dem angegebenen Single-Qubit-Operator an diesem Index und `PauliI` an jedem anderen Index zurück.

```qsharp
function EmbedPauli (pauli : Pauli, location : Int, n : Int) : Pauli[]
```


## <a name="input"></a>Eingabe

### <a name="pauli--pauli"></a>Pauli: [Pauli](xref:microsoft.quantum.lang-ref.pauli)

Ein Single-Qubit-Pauli-Operator, der an der angegebenen Position platziert werden soll.


### <a name="location--int"></a>Speicherort: [int](xref:microsoft.quantum.lang-ref.int)

Ein Index `output[location] == pauli` , bei dem `output` die Ausgabe dieser Funktion ist.


### <a name="n--int"></a>n: [int](xref:microsoft.quantum.lang-ref.int)

Länge des Arrays, das zurückgegeben werden soll.



## <a name="output--pauli"></a>Ausgabe: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]

