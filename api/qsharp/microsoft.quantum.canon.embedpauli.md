---
uid: Microsoft.Quantum.Canon.EmbedPauli
title: Embedpauli-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: EmbedPauli
qsharp.summary: Given a single-qubit Pauli operator and the index of a qubit, returns a multi-qubit Pauli operator with the given single-qubit operator at that index and `PauliI` at every other index.
ms.openlocfilehash: 0e6a93e22ee495abcc44bdf522e7c72c0981308b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840537"
---
# <a name="embedpauli-function"></a>Embedpauli-Funktion

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


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



## <a name="example"></a>Beispiel

So rufen Sie das Array ab `[PauliI, PauliI, PauliX, PauliI]` :

```qsharp
EmbedPauli(PauliX, 2, 3);
```